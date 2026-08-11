# scoop-bucket

[Scoop](https://scoop.sh) bucket for JCHSoft tools — the Windows install channel.

```powershell
scoop bucket add jchsoft https://github.com/jchsoft/scoop-bucket
scoop install mcptask_runner
```

## What is in here

| Manifest | What it is |
| --- | --- |
| `mcptask_runner` | the [mcptask](https://mcptask.online) runner — drives Claude Code through the tasks on mcptask.online |

Both Windows architectures are covered: `64bit` (amd64) and `arm64`. Scoop picks
the right one and verifies the download against the hash in the manifest.

## Do not edit the manifests

They are generated and pushed by [goreleaser](https://goreleaser.com) when a
release is cut, so an edit here is overwritten by the next release. Version,
URLs and hashes come from `.goreleaser.yaml` in the (private) source repository;
the binaries live in
[jchsoft/mcptask-releases](https://github.com/jchsoft/mcptask-releases).

Not on Windows? Use the install script instead:

```bash
curl -fsSL https://github.com/jchsoft/mcptask-releases/releases/latest/download/install.sh | sh
```

---

Proprietary — © JCHSoft. All rights reserved.
