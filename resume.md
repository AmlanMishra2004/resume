# [FILL IN: Your Full Name]

[FILL IN: City, Country] | [FILL IN: email] | [FILL IN: phone] | [FILL IN: LinkedIn URL] | [FILL IN: GitHub URL]

## Summary
[FILL IN: 2-3 sentences — who you are, what you work on, what you're looking for]

## Education
**[FILL IN: Degree, Major]** — [FILL IN: University Name]
[FILL IN: Start Year] – [FILL IN: End Year] | [FILL IN: GPA/honors, if relevant]

## Experience
**[FILL IN: Job/Role Title]** — [FILL IN: Company/Org]
[FILL IN: Start Date] – [FILL IN: End Date]
- [FILL IN: Accomplishment/responsibility, quantified if possible]
- [FILL IN: Accomplishment/responsibility, quantified if possible]

**[FILL IN: Job/Role Title]** — [FILL IN: Company/Org]
[FILL IN: Start Date] – [FILL IN: End Date]
- [FILL IN: Accomplishment/responsibility, quantified if possible]

## Projects
**[FILL IN: Project Name]** — [FILL IN: one-line description] ([FILL IN: repo/demo link])
- [FILL IN: what you built, tools used, outcome/impact]

**Diagnosed and proposed a fix for a config-precedence bug in OpenAI Codex CLI's sandbox permissions system** — [openai/codex#40339](https://github.com/openai/codex/issues/40339)
- Root-caused a silent failure where documented `[sandbox_workspace_write]` network/filesystem settings are dropped without warning once a named permissions profile is active, breaking `git`/network operations with no diagnostic
- Wrote and verified a fix (Rust) adding a startup warning for the ignored-config case, with regression tests; posted as a suggested patch per the project's contribution policy

**Fixed a column-rename compatibility bug in torchxrayvision's NIH_Dataset (mlmed/torchxrayvision)** — [PR #190](https://github.com/mlmed/torchxrayvision/pull/190) (merged)
- Found that NIH's officially distributed CSV renamed `Patient Gender` to `Patient Sex`, causing a `KeyError` when loading a fresh download into `NIH_Dataset` (library's bundled copy still used the old name)
- Added column-name normalization so both versions load correctly; added a regression test and verified no regression against the existing bundled CSV

**Added CheXlocalize dataset support to torchxrayvision (mlmed/torchxrayvision)** — [PR #191](https://github.com/mlmed/torchxrayvision/pull/191) (merged)
- Identified that the library's existing CheXpert loader can't read CheXlocalize's official blinded test set — it assumes demographic columns that are deliberately omitted, and infers train/val split by string-matching the CSV path — confirmed the failure against the real dataset
- Implemented and tested a new `CheXlocalize_Dataset` class (COCO-RLE segmentation mask support included), verified against the real ~5GB download on a research cluster; opened the required pre-PR issue and PR per the project's contribution process
- After the maintainer reported a load failure on the real validation set, root-caused and fixed a folder-naming mismatch between CheXpert's and CheXlocalize's own releases of the same images, plus a silent bug where segmentation masks for one pathology never attached due to a naming inconsistency in CheXlocalize's own data (cross-checked against the CheXlocalize paper); added a guard against a separate silent-failure mode and regression tests for all of it

**Renamed torchxrayvision's VinBrain_Dataset to VinDr_Dataset (mlmed/torchxrayvision)** — [PR #193](https://github.com/mlmed/torchxrayvision/pull/193) (merged)
- Fixed a long-standing misnaming (open issue #51): the class loads VinDr-CXR, released by VinBigData, but was named after VinBrain, a different Vingroup company, making the dataset hard to find
- Renamed the class while keeping `VinBrain_Dataset` as a backward-compatible alias so existing user code keeps working; updated README, Sphinx docs, scripts, and benchmarks, and added an alias regression test

## Skills
- **Languages:** [FILL IN]
- **Tools/Frameworks:** [FILL IN]
- **Other:** [FILL IN]
