# Installation

## Prerequisites

Before installing MetaHuman Playable, ensure you have:

1. **Unreal Engine 5.x** installed
2. **MetaHuman Plugin** — installed and enabled in your project
3. **IKRig Plugin** — enabled (comes with UE5 by default)
4. **Editor Scripting Utilities Plugin** — enabled
5. A **Third-Person Character Blueprint** template in your project (e.g., `BP_ThirdPersonCharacter`)

## Install the Plugin

1. Download the MetaHuman Playable plugin
2. Copy the `MetaHumanPlayable` folder into your project's `Plugins/` directory:

```
YourProject/
└── Plugins/
    └── MetaHumanPlayable/
        ├── MetaHumanPlayable.uplugin
        └── Source/
```

3. Restart the Unreal Editor
4. The plugin is **enabled by default**. You can verify in **Edit > Plugins > MetaHuman** category

## Verify Installation

Once installed, you should see:

- A log message: `MetaHumanPlayable plugin loaded` in the Output Log
- The **"Make Playable Character"** option when right-clicking a MetaHuman Blueprint in the Content Browser
