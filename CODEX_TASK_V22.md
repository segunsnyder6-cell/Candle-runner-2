# CandleRun V22 Codex Task

Use this file together with GitHub issue #1.

## Source of truth

The newest source is Segun's uploaded file in ChatGPT: `CandleRun V21 GOAT trading game(1).html`.

Expected metadata:

- Title: `CandleRun V21 — Trading Simulator Game`
- Approx size: `492,349 bytes`
- Approx lines: `6,802`

Before patching, replace/update repo `CandleRun.html` from that newest V21 file. The repo currently had older builds, so do not accidentally patch an old V9/V12 build.

## Repo expectations

- Final playable file: `CandleRun.html`
- Launcher: `Play Now.html`
- Keep RawGithack launch working through the launcher and direct game file.
- Preserve single-file HTML structure.
- No React rebuild.
- No external dependencies.

## Required V22 fixes

1. Fix Profile hero `Joined...` pill clipping on iPhone.
2. Fix Auto Risk TP/SL layout so SL no longer overflows its cockpit module.
3. Make fullscreen dock controls more premium while keeping the current useful layout.
4. Root-cause and fix repeated pending-entry cycles causing buttons to stop responding.
5. Add real scrollable history for all timeframes, especially 30m and higher.
6. Add a macro synthetic market layer so long Warp runs produce realistic long-term movement across wider ranges.
7. Update stale version labels to V22 consistently.
8. Make localStorage failure graceful with guest-session warning.

## Required verification

- Run JS syntax check with `node --check` on extracted script.
- Open in mobile viewport.
- Verify `Play Now.html` opens the updated `CandleRun.html`.
- Verify Profile joined pill is fully visible.
- Verify Auto Risk TP/SL is fully contained.
- Verify 30m/1H/4H/1D have scrollable history.
- Repeat pending-order flow 10+ times without losing button clickability.

## Changelog requested

When complete, include:

- Visual fixes made
- Interaction-lock fix explanation
- Timeframe history fix explanation
- Market realism upgrade explanation
- Tests performed
- Remaining limitations
