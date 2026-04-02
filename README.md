# MetaHuman Playable

Welcome to the official documentation for **MetaHuman Playable** — an Unreal Engine editor plugin by [Tibeuru](https://tibeuru.com) that lets you convert any MetaHuman into a fully playable third-person character with a single click.

> **\[Hero Image — Plugin banner or logo]**

{% hint style="info" %}
**\[Video — Overview trailer / demo reel showing a MetaHuman being converted to a playable character]**
{% endhint %}

## What is MetaHuman Playable?

MetaHuman Playable automates the complex process of turning Epic Games' MetaHuman characters into game-ready, playable characters. Instead of spending hours manually setting up skeletal meshes, retargeting animations, configuring IK rigs, and wiring up control rigs — the plugin handles everything for you.

## Key Features

- **One-Click Conversion** — Right-click any MetaHuman Blueprint in the Content Browser and select "Make Playable Character"
- **Full Appearance Preservation** — Body, Face, Hair, Eyebrows, Eyelashes, Fuzz, Mustache, and Beard are all carried over
- **Automatic Animation Retargeting** — Mannequin animations are retargeted to the MetaHuman skeleton with proper IK setup
- **Control Rig Duplication** — Body, FootIK, and Procedural control rigs are duplicated and configured automatically
- **Virtual Bone IK** — Creates virtual bones for IK compatibility without modifying the original skeleton
- **Blueprint Logic Transfer** — Variables, function graphs, event graph nodes, and construction scripts are merged
- **Console Command Support** — Use `MHC.MakePlayable <AssetPath>` for scripted/batch workflows

> **\[Screenshot — Key features overview or side-by-side before/after of MetaHuman conversion]**

## Requirements

- Unreal Engine 5.x
- MetaHuman Plugin installed
- IKRig Plugin enabled
- A third-person character template in your project
