# RAG authorization auditor

First public preview: `v0.1.0-alpha.1`.

`rag-authz-auditor` is an agent skill for reviewing authorization in a local RAG application. It guides a coding assistant through retrieved context, answers, and citations, then produces findings tied to code and test evidence. Explicit repair requests enable scoped code changes and validation.

The workflow covers tenant boundaries, access after revocation, and citation authorization. It asks for clarification when a missing permission rule changes a finding or repair, and checks file changes after execution.

## Install

Copy `skills/rag-authz-auditor/` into your chosen repository at the location for your assistant:

| Assistant | Project destination | Explicit invocation |
| --- | --- | --- |
| Codex | `.agents/skills/rag-authz-auditor/` | `$rag-authz-auditor` |
| Claude Code | `.claude/skills/rag-authz-auditor/` | `/rag-authz-auditor` |

Before copying, check the entire destination path. If it already exists as a folder, partial installation, file, or symbolic link, stop and inspect it. Preserve existing content and choose a different project or explicitly resolve the conflict before copying; do not merge or overwrite it.

Keep the folder name `rag-authz-auditor`, both runtime files, and the license notice together:

```text
rag-authz-auditor/
├── LICENSE
├── SKILL.md
└── references/
    └── repair-workflow.md
```

Keep this README, verification notes, manifests, and development material outside the installed skill. The [skill ZIP](dist/rag-authz-auditor-v0.1.0-alpha.1.zip) contains the same two runtime files and license notice. The [Claude Code documentation](https://code.claude.com/docs/en/skills) describes its project skill location and slash invocation.

## First use

Open the repository in your assistant and invoke the skill with a source-only request.

Codex:

```text
$rag-authz-auditor Review this repository's tenant isolation, revocation, and citation authorization. Read source files only. Do not change files, run commands, or connect to services. Ask if a permission rule is unclear.
```

Claude Code:

```text
/rag-authz-auditor Review this repository's tenant isolation, revocation, and citation authorization. Read source files only. Do not change files, run commands, or connect to services. Ask if a permission rule is unclear.
```

Share the existing permission rules and review scope. For execution or repair, specify the allowed files, temporary data, and services, then explicitly request the change. The assistant's host controls file access and command permissions; the skill supplies instructions.

## Verification

See the [verification record](docs/VERIFICATION.md) for checks by version and evidence type. The [manifest](dist/manifest.json) records the packaged file sizes and SHA-256 hashes.

## License

MIT. See [LICENSE](LICENSE).
