# How It Works

## Architecture Overview

MetaHuman Playable works by combining three core operations: component cloning, hierarchy setup, and blueprint logic transfer.

## Component Cloning

The plugin identifies all visual components from the MetaHuman Blueprint:

| Component      | Description                                  |
| -------------- | -------------------------------------------- |
| **Body**       | The main skeletal mesh with the MetaHuman's body |
| **Face**       | Facial skeletal mesh for expressions         |
| **Hair**       | Hair groom component                         |
| **Eyebrows**   | Eyebrow groom                                |
| **Eyelashes**  | Eyelash groom                                |
| **Fuzz**       | Peach fuzz groom                             |
| **Mustache**   | Mustache groom (if present)                  |
| **Beard**      | Beard groom (if present)                     |

These are cloned into the playable character with their full property sets preserved, including materials and mesh references.

## Component Hierarchy

The playable character uses this component hierarchy:

```
CharacterMesh0 (native UE mesh — hidden)
└── Body (MetaHuman skeletal mesh + retargeted AnimBP)
    └── Face (MetaHuman face mesh)
        ├── Hair
        ├── Eyebrows
        ├── Eyelashes
        ├── Fuzz
        ├── Mustache
        └── Beard
```

The native `CharacterMesh0` is hidden and cleared. The MetaHuman **Body** component becomes the primary visual mesh with animations.

## Blueprint Logic Transfer

The plugin transfers Blueprint logic from the MetaHuman source:

- **Variables** — All Blueprint variables not already present in the template are copied
- **Function Graphs** — Custom functions (excluding EventGraph and ConstructionScript) are cloned
- **Event Graph Nodes** — Merged into the destination EventGraph with automatic Y-offset to prevent overlap
- **Construction Script Nodes** — Merged similarly, skipping function entry nodes
