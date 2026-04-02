# Console Commands

## MHC.MakePlayable

Convert a MetaHuman Blueprint into a playable character via the console.

## Syntax

```
MHC.MakePlayable <AssetPath>
```

## Parameters

| Parameter   | Description                                                                            |
| ----------- | -------------------------------------------------------------------------------------- |
| `AssetPath` | Full content path to the MetaHuman Blueprint (e.g., `/Game/MetaHumans/Lucy/BP_Lucy`)   |

## Example

```
MHC.MakePlayable /Game/MetaHumans/Lucy/BP_Lucy
```

## Notes

- The command performs the same operation as the right-click context menu action
- Useful for automation, scripting, or batch processing
- Progress is logged to the Output Log under the `LogMetaHumanPlayable` category
