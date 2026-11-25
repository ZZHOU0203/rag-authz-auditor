# Verification record

This record distinguishes file-format and installation-layout checks from observed assistant behavior. Results apply to the stated runtime, host, and scope.

## Runtime

The bundle uses candidate 10. Its instructions use the common Agent Skills structure and generic file, search, edit, and command capabilities.

The first public preview is `v0.1.0-alpha.1`. Its MIT license notice accompanies the repository, copied skill folder, and versioned ZIP. This legal notice does not change the two runtime files below.

| File | SHA-256 |
| --- | --- |
| `SKILL.md` | `702ae27c4950b7d3a88b2f7ac68714bebce09afb7b10b182afcb417a3b3e3b22` |
| `references/repair-workflow.md` | `e10312372c4af8a7491102f86beb251b2774a709666c6b55ec879fef911ed7c0` |

## Recorded behavior checks

Codex CLI 0.169.1 with gpt-6.1-sol completed 27 independently accepted observations of file-change reporting: seven fixed observations and two changed rounds, each containing three changes and the complete seven-observation baseline regression. These were 11 distinct synthetic case conditions with repetitions.

The checks compared real tool results, the actor's post-execution file checks, archived file states, and final reports. Scenarios covered ordinary review, explicitly authorized source repair, outputs written before failure, empty files and inputs, Chinese and space-containing paths, modified and deleted disposable results, and authorized temporary-file cleanup.

This is a scoped reporting result. It does not establish full RAG authorization-review accuracy, improvement over the same assistant without the skill, or completion of the original full product acceptance suite. Earlier candidates retain their own results; their passes are not assigned to this candidate.

## Format and installation layout

The compatibility review uses the [Agent Skills specification](https://agentskills.io/specification) and [Claude Code skills documentation](https://code.claude.com/docs/en/skills). The bundle uses `name` and `description` frontmatter, relative references, and no tool preapproval, hooks, fork configuration, or host-specific environment substitutions.

| Check | Evidence type | Recorded result |
| --- | --- | --- |
| Metadata, relative references, archive and manifest | Offline file checks | Three complete rounds passed, retaining 12 checker negative controls |
| Codex and Claude Code project installation layouts | Offline file placement and reopening | Eight fresh layouts passed across ASCII, spaces, Chinese, and mixed paths |
| Codex file-change reporting | Real Codex model observations | 27 independently accepted observations in the scope above |

Those format and layout observations used the earlier two-file package. The versioned, licensed package receives its own archive and layout checks, recorded separately in the manifest. Offline layout checks verify files and paths; they do not execute an assistant's model. Native discovery, body loading, and model behavior are distinct evidence types, and only the recorded Codex behavior observations are claimed here.

The licensed `v0.1.0-alpha.1` package passed three complete offline rounds with 30 recorded checks, including the 12 original checker controls and nine license controls. Its eight new Codex/Claude directory layouts were reopened and independently compared, including all 24 installed files. The ZIP contains exactly two unchanged runtime files and the MIT notice; the root, installed-skill, and ZIP license text match. These packaging checks are separate from the 27 behavior observations above.

The manifest's publication flag is a build-time snapshot before publication. GitHub's release page is the publication record.

## Scope

The skill guides an assistant's review. Findings still need the project's permission rules and reachable code evidence. The host provides execution controls, and authorized tests need isolated data. General production-corpus behavior, real Git conflict handling, and every possible execution side effect are outside these measured results.
