# Nexus Core — recovered source entrypoint

The standalone `Nexus_Core` repository previously contained only `DEVIN_ACCESS.md`. Its actual implementation was found in `afterburn25/Coding_Agent` (a separate active repository). **Do not treat this as a source rewrite or merge.**

## Source linked here

The `source/` directory is a **Git submodule** targeting:

- Repository: https://github.com/afterburn25/Coding_Agent
- Exact commit: `40423960d92e8ec06bf04bcf21a9e4a6a183ac27`
- Recorded version: `0.42.0` in `VERSION`
- Git snapshot inventory: 1,393 tracked files, including the full Python `localcodeagent/` source tree, `tests/`, web and desktop interfaces, scripts, workflows and docs.

To fetch the pinned source after cloning this repository:

```powershell
git clone --recurse-submodules https://github.com/afterburn25/Nexus_Core.git
```

Existing clones can run `git submodule update --init --recursive`.

**Important**: Until this recovery PR is merged, clone the recovery branch specifically (`git clone --branch recovery/link-coding-agent-source-20261103 --recurse-submodules ...`). The submodule is pinned to historical code; development changes belong in `Coding_Agent` and require a deliberate pointer update here. It is not a self-contained source migration and is not proof of tests or current deployment.

## Recovery next steps

1. Compare `D:\Devin\chat-nexus` and other local workspaces/archives to Git commit `40423960` before selecting the next release baseline.
2. Decide whether to keep `Coding_Agent` as the canonical development repository with a lightweight Nexus Core entrypoint, or perform a complete audited source migration later.
3. Maintain provenance, never overwrite either original repository or force-push history.
