# Ascension Unreal Client

`AscensionUE57` is the playable Unreal Engine 5.7 client for **Ascension: The Ascended Realms**.

Remote:

```text
https://github.com/dthornton5280-blip/ascension-ue57
```

## Boundaries

- `D:\Projects\Ascension` remains authoritative for canon, rules, creator/GM tools, backend contracts, secrets and durable campaign state.
- `D:\UnrealProjects\AscensionUE57` owns live visual gameplay, map presentation, local movement, tactical display and later GAS execution.
- `D:\UnrealAssets\AssetDump` is the only location for full Marketplace/Fab pack imports.
- Do not copy full asset packs or arbitrary `.uasset` files into this project. Migrate reviewed assets from AssetDump through Unreal.

## Starting Foundation

- Template baseline: Top Down Blueprint, Strategy variant.
- Keep template `TopDown` and `Variant_Strategy` content as reference until Ascension replacements are proven.
- Production maps and systems live under `Content/Ascension`.
- Hardware ray tracing is disabled for practical development on the RTX 3050 Ti laptop GPU. This does not limit gameplay features.

## Source Control Scope

This repo currently tracks the Ascension-owned playable baseline:

- `AscensionUE57.uproject`
- `Config/**`
- `Content/Ascension/**`
- source-control docs and Git LFS rules

Large imported/template folders are currently local-only and ignored until Stephen approves the LFS asset scope. See:

```text
SOURCE_CONTROL_SCOPE.md
DEPENDENCIES.md
```

Do not assume a fresh clone contains every local visual pack. If a map opens with missing visuals, check `DEPENDENCIES.md` before reimporting anything.

## Content Conventions

| Asset Type | Prefix |
| --- | --- |
| Levels | `LVL_` |
| Blueprints | `BP_` |
| Blueprint interfaces | `BPI_` |
| Widgets | `WBP_` |
| Data assets | `DA_` |
| Gameplay abilities | `GA_` |
| Gameplay effects | `GE_` |
| Gameplay cues | `GC_` |
| Data tables | `DT_` |
| StateTrees | `ST_` |
| Smart Objects | `SO_` |
| PCG graphs | `PCG_` |
| Materials / instances | `M_` / `MI_` |
| Niagara systems | `NS_` |

## First Gameplay Proof

Create editor-authored assets under `Content/Ascension`, beginning with:

`Content/Ascension/World/Dungeons/LVL_MoonGateUnderworks`

The first proof should establish one authorized player-controlled actor, one tactical encounter area, a five-foot tactical grid (`152.4` Unreal centimeters), one obstruction or cover object, one hazard cell and one Training Shade encounter.

## Current Next Step

Continue the Moon Gate Underworks encounter bridge:

1. Add `bInEncounter` to `BP_TrainingShade_Prototype`.
2. Set it true from `BP_MoonGateEncounterTrigger` when combat starts.
3. Replace the temporary `Combat Started` print later with a real encounter-state signal.
