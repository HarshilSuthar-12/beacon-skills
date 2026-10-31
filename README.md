# beacon-skills

Skill packs for the Beacon IT support agent (TrueForge).

Each directory is one skill: a `SKILL.md` with YAML frontmatter (`name`,
`description`) and a markdown body. Register each one separately in
**Settings → Skills → Import from GitHub**, pointing `path` at the directory
and pinning `ref` to a tag.

| skill | covers | share of resolved queue |
|---|---|---|
| `access-request` | access to an app, group, site or licence | ~22% |
| `onboarding` | new hire and new contractor setup | ~15% |
| `offboarding` | leavers, terminations, contract end | ~7% |
| `email-collaboration` | mail, distribution lists, Teams, shared mailboxes | ~7% |
| `okta-tile` | missing or wrong Okta dashboard tiles | ~3% |

Together these cover a little over half of all resolved tickets.

## What is deliberately not here

This repository is public. It contains **no** ticket keys, personal names,
email addresses, real group names, domain names or host names. Procedures
refer to systems generically (`<identity-provider-group>`, `<prod-domain>`).

The concrete values — group naming conventions, OU paths, domains, approver
lists — belong in the agent's own configuration or a private reference the
agent reads at runtime, never in this repo.

## Provenance

Procedures were distilled from the resolution history of ~3,600 resolved
tickets. They describe what was actually done, not what a policy document
says should be done. Where the two disagree, the policy wins and the playbook
needs updating.
