# SME_PLANS | Docs + HyperFrames

## COMMANDS
- Status: `git status --short --branch`
- Search: `rg "<text>" docs enterprise-hub-story-video`
- Video check: `cd enterprise-hub-story-video && npm run check`
- Video render: `cd enterprise-hub-story-video && npm run render`

## STRUCTURE
- `docs/` - client-facing AI efficiency docs, architecture notes, context records.
- `docs/01_会议需求完整清单.md` - full demand list from meetings.
- `docs/02_AI提效落地方案.md` - implementation plan for business readers.
- `docs/麦家小馆AI提效方案.html` - shareable HTML presentation.
- `docs/context/` - product design context and Q&A notes for 企业资料中枢.
- `docs/adr/` - architecture decisions.
- `enterprise-hub-story-video/` - HyperFrames video source and final MP4.

## PATTERNS
- Keep business-facing docs plain Chinese, concrete, and low-jargon.
- Treat `enterprise-hub-story-video/enterprise-hub-story-video.mp4` as the committed final export.
- Do not commit generated intermediates: `**/renders/`, `**/frame-checks/`, `.DS_Store`.
- For HyperFrames work, follow `enterprise-hub-story-video/AGENTS.md` and `DESIGN.md`.

## DOMAIN
| Term | Definition |
|------|------------|
| 企业资料中枢 | Central catalog for company files, datasets, reports, events, knowledge, and skill listings. |
| 通用智能体 | Codex/OpenClaw-like agent used by employees to query/upload/analyze data. |
| Skill | Reusable agent workflow; listed/distributed by the hub but executed by employee agents. |
| 归属标签 | Access label such as store or employee identity; any matching label grants access. |

## SECURITY
- Do not commit secrets, `.env*`, credentials, customer private exports, or real access tokens.
- Keep deleted records as inactive metadata; do not assume OSS/source files are physically deleted.

## GIT
- Current work branch: `NF-0000`.
- Commit format: short imperative summary, e.g. `Update enterprise hub use cases`.
