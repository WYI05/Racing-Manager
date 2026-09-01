# Pitwall

Multi-race pit-wall manager for endurance karting: pre-race strategy building and
live race data. Ships with one seeded race (the SWS Endurance Cup 3-hour at Vegas
Superkarts, September 5, 2026) whose team details live in the race data, not in
the product.

Live site: https://wyi05.github.io/Racing-Manager/

## `index.html` — Pitwall (any race)

Self-contained app, no build step, no backend. Data is kept in `localStorage`
with JSON **Export/Import** to move it between phones.

- **Multi-race**: create/switch/delete races; the Vegas 2026 event ships pre-seeded.
- **Setup**: event, track, date, green-flag time, stint count/length, driver roster.
- **Strategy**: tap-to-assign stint plan with rotation presets and consecutive-stint
  warnings, target lap/finish, strategy notes — one tap pushes the plan into the
  Race tab.
- **Quali**: per-driver lap logging with automatic best; grid position.
- **Race**: stint table (driver, kart #, positions in/out, best lap, notes),
  per-stint lap logger, a stint countdown with pit-board prompts (5:00 / 3:00 /
  IN NOW), and a lap stopwatch that logs straight into a stint.
- **Rivals**: competitor teams with per-stint positions and a position-trace chart.
- **Analysis**: best/avg/σ tiles, per-driver table, lap-time chart with stint
  boundaries.

## `vegas-race-book.html` — Vegas strategy book

The original single-page race book (open it directly, no build step):

- **Deadline panel** — live countdowns to the real cutoff (payment + full driver
  registration by **Sep 4, 4:00 PM PT**) and the green flag.
- **Format breakdown** — 9 × 20 min stints, kart rotation every stint, ballast,
  no radios, and what that implies strategically.
- **Interactive stint planner** — tap stints to assign drivers, with presets and
  consecutive-stint warnings. Saved in `localStorage`.
- **Signal book** — pit-board vocabulary and hand signals for the no-radio rule.
- **Rotation choreography, qualifying plan, heat/ballast prep.**
- **Track question list** — the strategy-critical rules the SWS regulation leaves
  to the organizer (call 702-405-7223).
- **Race-week checklist** — persisted per device.

## Sources

- Event sheet for `US-VEG-142967` (timing, price, ballast, kart model).
- SWS Official Regulation 2026 (Sodi W Series, last update Jan 27, 2026) — DIN /
  team registration rules, ghost-driver scoring, Endurance Cup points, and
  International Finals eligibility.
