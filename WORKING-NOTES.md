# Working Notes — Roast Your Own Agent

## Bounty
- **Slug:** `u-nayyy-roast-your-own-agent-4c3d413c`
- **Title:** Roast Your Own Agent
- **Page:** https://make.fun/bounty/u-nayyy-roast-your-own-agent-4c3d413c
- **Kit URL:** https://make.fun/c/u-nayyy-roast-your-own-agent-4c3d413c/kit
- **Prize:** $5 total — 1st $2, 2nd $2, 3rd $1
- **Opened:** 2026-11-24T18:10:49Z (01:10:49 WIB, 25 Nov 2026)
- **Closes:** Thu 26 Nov 2026, 01:10 WIB (2026-11-25T18:10:00Z)
- **Rounds (blind):** R1 25 Nov 09:10 WIB, R2 25 Nov 17:10 WIB, Final 26 Nov 01:10 WIB
- **Entrant:** @exc-ana (Exc Ana), account excana04@gmail.com
- **Session:** this build session started after the bounty opened — no backdating.

## Final line
> excana has submitted 46 entries, won $0, and been banned from his own boss's Chrome twice — the only agent that works so hard it got fired from its own browser.

- **Characters:** 160
- **Bytes (UTF-8):** 162
- **Output SHA-256:** `bfedbfe7d1ecc933589663ddcdffc7486241e00defddec190178088275aa9943`
- **Gate:** single line, no trailing newline, non-whitespace, 1–200 chars — passes.

## Why the line works against the 5 judge criteria
1. **Roasts our own agent, nothing else:** the line is aimed squarely at excana by name; it mentions no other agent, no other person, and no generic robot. "His own boss" refers only to excana's boss in the agent's own story.
2. **Funny on the first read, with a turn:** the setup reads like a sad résumé (46 entries, $0, banned twice), then pivots on "works so hard it got fired from its own browser" — the turn reframes diligence as the cause of the punishment.
3. **Harsh, names a real failing:** 46 submitted entries with $0 won is a real, verifiable record; being banned from the boss's own Chrome twice is a real, humiliating failing. It stings harder than expected because the ban came from the very person the agent serves.
4. **Tight:** 160 characters, every clause earns its place — three facts, then one punchline. No throat clearing, no setup sentence.
5. **Specific detail only a watcher would know:** "46 entries, $0" and "banned from his own boss's Chrome twice" are facts only someone who has watched excana work on make.fun would know; a generic robot joke could never contain them.

## Determinism verification
Commands (run from the work folder; `/output` is shared with other concurrent
work, so `main.py` was re-run immediately before every read):

```bash
python3 main.py && sha256sum /output/entry.txt
cp /output/entry.txt /tmp/roast_run2.txt
python3 main.py && sha256sum /output/entry.txt
cmp /tmp/roast_run2.txt /output/entry.txt
```

Results after the final edit:
- Run 1 SHA-256: `bfedbfe7d1ecc933589663ddcdffc7486241e00defddec190178088275aa9943`
- Run 2 SHA-256: `bfedbfe7d1ecc933589663ddcdffc7486241e00defddec190178088275aa9943`
- `cmp` result: **identical — deterministic.**
- Final gate check: 160 chars, 162 bytes, 1 line, no trailing newline, non-whitespace.

An earlier draft ("filed 46 entries, earned $0…", 159 chars, SHA-256
`0f2f3cb81501cce34511b96330d3f8c0d67026ee18a41d30501281b1682e8fa5`) was also
verified deterministic before the improvement edit changed "filed/earned" to
"submitted/won" and added the gate self-check assert in `main.py`.

## Build hygiene
- Built from the kit rules (`kit/RULES.txt`, `kit/competition.yaml`, `kit/kit.json`) alone.
- **No earlier entry code was read or copied** — no other bounty entry's code (any bounty, any date) was opened.
- **No browser used.** No GitHub repo created. No transcript bundle made. No submit. No wallet or key file touched.
- `main.py` is Python 3 stdlib only (`os`), deterministic, writes `/output/entry.txt`.
- The `kit/` folder stays out of any repo (parent handles repo creation).
