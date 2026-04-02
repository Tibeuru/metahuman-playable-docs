# Getting Started

## Your First Playable MetaHuman

Follow these steps to convert a MetaHuman into a playable character.

## Step 1: Import a MetaHuman

If you haven't already, import a MetaHuman into your project using **Quixel Bridge** or **MetaHuman Creator**.

## Step 2: Set Up a Template

The plugin needs a third-person character template to use as the base. It automatically searches these paths:

| Priority | Path                                                  |
| -------- | ----------------------------------------------------- |
| 1        | `/Game/MHC/Blueprints/BP_MHC_ThirdPersonCharacter`    |
| 2        | `/Game/ThirdPerson/Blueprints/BP_ThirdPersonCharacter` |
| 3        | `/Game/Characters/BP_ThirdPersonCharacter`             |

If you're using the default UE5 Third Person template, the plugin will find it automatically.

## Step 3: Convert the MetaHuman

1. Open the **Content Browser**
2. Navigate to your MetaHuman Blueprint (e.g., `BP_Lucy`)
3. **Right-click** the Blueprint
4. In the context menu, find the **MetaHuman** section
5. Click **"Make Playable Character"**

## Step 4: Wait for Processing

The plugin will show a progress dialog as it:

1. Duplicates the template character
2. Clones MetaHuman visual components
3. Copies Blueprint variables and logic
4. Retargets all Mannequin animations
5. Sets up IK Rigs and Control Rigs
6. Compiles and saves everything

## Step 5: Use Your Playable MetaHuman

Once complete:

- The new Blueprint opens automatically in the editor
- It's saved as `<MetaHumanName>_Playable` next to the original
- It's ready to drop into your level as a playable character
