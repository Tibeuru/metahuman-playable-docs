# Troubleshooting

## "Make Playable Character" option doesn't appear

**Cause:** The selected Blueprint is not recognized as a MetaHuman.

**Solution:** The plugin checks for `Body` and `Face` SkeletalMeshComponents in the Blueprint's Simple Construction Script. Ensure your MetaHuman was imported correctly with these components.

## "Playable template not found" notification

**Cause:** The plugin couldn't find a third-person character template.

**Solution:** Ensure one of these Blueprints exists in your project:

- `/Game/MHC/Blueprints/BP_MHC_ThirdPersonCharacter`
- `/Game/ThirdPerson/Blueprints/BP_ThirdPersonCharacter`
- `/Game/Characters/BP_ThirdPersonCharacter`

If your template is elsewhere, move or duplicate it to one of these paths.

## Animations don't play on the playable character

**Cause:** The animation retargeting may have failed to find Mannequin source animations.

**Solution:**

1. Ensure Mannequin animations exist at `/Game/Characters/Mannequins/Anims/`
2. Check the Output Log for `LogMetaHumanPlayable` errors
3. Verify the IKRig plugin is enabled

## Control Rig errors after conversion

**Cause:** Control Rig references may not have updated correctly.

**Solution:**

1. Open the retargeted AnimBlueprint
2. Check that ControlRig nodes reference `CR_MHC_<Name>_*` classes, not the original Mannequin ones
3. Recompile the AnimBlueprint

## Character mesh appears T-posed

**Cause:** The AnimBlueprint class wasn't assigned to the Body component.

**Solution:**

1. Open the playable Blueprint
2. Select the `Body` component
3. Verify `Anim Class` is set to the retargeted AnimBlueprint (`ABP_MHC_<Name>_Unarmed`)

## Output File Structure

After conversion, the following assets are created:

```
<MetaHuman Location>/
├── <Name>_Playable          (Playable Blueprint)
├── Anims/
│   └── Unarmed/
│       ├── ABP_MHC_<Name>_Unarmed
│       ├── MM_MHC_<Name>_*
│       ├── MF_MHC_<Name>_*
│       ├── BS_MHC_<Name>_*
│       └── AO_MHC_<Name>_*
└── Rigs/
    ├── IKRig_Mannequin
    ├── IKRig_<Name>
    ├── RTG_Mannequin_to_<Name>
    ├── CR_MHC_<Name>_Body
    ├── CR_MHC_<Name>_FootIK
    └── CR_MHC_<Name>_Procedural
```

## Getting Help

- **Website:** [tibeuru.com](https://tibeuru.com)
- **Documentation:** [docs.tibeuru.com/plugins](https://docs.tibeuru.com/plugins)
