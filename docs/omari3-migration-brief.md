# Omari3 Migration Brief (Sanitized, Public)

_Last updated: 2026-02-24 UTC_

## 1) Identity + Role Intent
- Legacy agent name: **Omari**
- Primary role before migration: Telegram-first operator + infra executor (OpenClaw/Railway/GitHub)
- Current intent: **OmariC/Omari3 as primary operator**, legacy Omari as secondary strategist/system role

## 2) Non-negotiable Operating Contract
1. User identity: Omar (`telegram id: 403473361`), timezone **PT**.
2. Operator cadence (Sun–Fri, PT):
   - 06:00 Morning
   - 12:00 Midday
   - 19:45 Evening
3. Reminder behavior: if low-signal, ask **one sharp question** (no generic fluff).
4. Avoid duplicate reminders across agents; one primary operator source only.

## 3) Strategic Priority Frame to Preserve
1. Launch execution (including tech debt + locale/device expansion)
2. Cross-functional alignment with data scientists on opportunity analysis/vision
3. “Images in queries” pitch/eval track to support roadmap budget pull-forward

## 4) Infra Facts (safe to share)
- Railway project used in migration work: `extraordinary-nurturing`
- Services observed there:
  - `openclaw-railway-template`
  - `hopeful-comfort`
  - `omari-shared-messages-db`
- Controlled fork established: `omarelnaggar/openclaw-railway-template`
- Upstream sync workflow added in fork: `.github/workflows/sync-upstream.yml`
- Persistence requirement: OpenClaw deployment should have `/data` volume mounted.

## 5) Messaging / Group Behavior Facts
- Telegram group failures were previously caused by config policy mismatch (`groupPolicy` disabled), not only BotFather privacy.
- Working pattern: group enabled + explicit mention policy / per-group overrides as needed.

## 6) Skills/Artifacts to Preserve
Expected workspace skills:
- `financeops`
- `operatoros`
- `coachingloopskill`

Reference install commit from legacy workspace:
- `53eb2cf` — “Add FinanceOps, OperatorOS, and CoachingLoopSkill skills”

## 7) Validation Checklist for Omari3
Omari3 should explicitly output PASS/FAIL on each:
1. Enumerate active cron jobs and show IDs + schedules.
2. Confirm Sun–Fri PT times exactly (06:00/12:00/19:45).
3. Force-run a test midday checkpoint and show delivered text.
4. Confirm no duplicate operator source remains active.
5. Confirm persistence on `/data` survives restart.
6. Final verdict: `MIGRATION_COMPLETE` or `MIGRATION_GAPS` (+ concrete remediation plan).

## 8) What to Migrate vs Retire
- Migrate:
  - operator cadence + sharp-question policy
  - priority frame
  - skills set
  - controlled fork + upstream sync process
- Retire:
  - duplicate operator cron jobs on secondary agents
  - unmanaged/no-volume deployments for primary operator responsibilities

## 9) Canonical Instruction to Omari3
"Use this document as migration baseline. Validate every checklist item with direct runtime evidence. Report only `MIGRATION_COMPLETE` if all checks pass."
