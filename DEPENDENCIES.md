# AscensionUE57 Dependencies

This repo intentionally tracks the Ascension-owned Unreal baseline first. It does not currently commit every local imported or template asset folder.

## Required Authority Repo

Design/runtime authority:

```text
https://github.com/dthornton5280-blip/ascension-the-ascended-realms
D:\Projects\Ascension
```

Use that repo for:

- rulebook and canon
- content JSON
- scene recipes
- backend/runtime contracts
- collaboration state and handoff docs

## Tracked Unreal Scope

Tracked in this repo:

- `AscensionUE57.uproject`
- `Config/**`
- `Content/Ascension/**`
- `.gitattributes`
- `.gitignore`
- `README_ASCENSION_CLIENT.md`
- `SOURCE_CONTROL_SCOPE.md`
- `DEPENDENCIES.md`

## Local-Only Visual/Template Folders

These folders exist locally on Stephen's machine but are currently ignored and not pushed:

- `Content/RuinedCrypt`
- `Content/ParagonGideon`
- `Content/Characters`
- `Content/Whisper`
- `Content/TopDown`
- `Content/Variant_Strategy`
- `Content/LevelPrototyping`
- `Content/Cursor`
- selected `Content/__ExternalActors__/TopDown`
- selected `Content/__ExternalActors__/Variant_Strategy`
- selected `Content/__ExternalObjects__/TopDown`
- selected `Content/__ExternalObjects__/Variant_Strategy`

Reason:

The full local `Config` plus `Content` footprint was about 8.8 GB when the repo was created, mostly from imported packs. Those assets should not be pushed blindly until Stephen approves:

- which Fab/Marketplace/template packs are required,
- which assets are licensed and approved for shared repo storage,
- how much Git LFS quota/storage should be used,
- whether packs belong in the Unreal repo, an asset vault, or local-only setup notes.

## Asset Intake Rule

Stage full Fab or Marketplace imports in:

```text
D:\UnrealAssets\AssetDump
```

Migrate only approved assets into:

```text
D:\UnrealProjects\AscensionUE57
```

Do not let PCG graphs, Fab kits, or imported demo content define canon, hidden knowledge, quest truth, or durable outcomes. They may dress approved scene recipes and improve the playable feel.

## Fresh Clone Warning

A fresh clone may open with missing visuals if current `Content/Ascension` assets reference local-only packs. Before fixing that by reimporting or committing large folders, check with Stephen and update this file with the chosen dependency strategy.

If a missing dependency becomes required for all collaborators, add the specific approved folder or asset set through Git LFS in a focused commit.
