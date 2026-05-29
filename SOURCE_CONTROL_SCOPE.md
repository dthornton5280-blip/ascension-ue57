# AscensionUE57 Source Control Scope

This local Git repo currently tracks the Ascension-owned Unreal baseline:

- project descriptor
- config
- source-control ignore and LFS rules
- `Content/Ascension/**`

Large imported or template asset folders are intentionally left local for now:

- `Content/RuinedCrypt`
- `Content/ParagonGideon`
- `Content/Characters`
- `Content/Whisper`
- `Content/TopDown`
- `Content/Variant_Strategy`
- `Content/LevelPrototyping`
- `Content/Cursor`

Reason:

The current full `Config` plus `Content` footprint is about 8.8 GB, mostly from imported packs. Those folders should not be pushed blindly until the Unreal GitHub repo, Git LFS quota, asset licensing posture, and first committed asset scope are all intentional.

The design/runtime authority remains:

```text
D:\Projects\Ascension
```

This Unreal project is the playable client and should consume rulebook, content, runtime, and scene-recipe truth from that repo.
