# Pitwall

Pit-wall strategy and timing app for any race: karts, cars, motorcycles, sim,
sprints, heats, or multi-hour endurance. Pre-race planning and live race data
in one page, with as many races as you like side by side. Ships with one seeded
race (the SWS Endurance Cup 3-hour at Vegas Superkarts, September 5, 2026) whose
team details live in the race data, not in the product.

Live site: https://wyi05.github.io/Racing-Manager/

## `index.html` — Pitwall

Self-contained app, no build step, no backend. Data is kept in `localStorage`
with JSON **Export/Import** to move it between phones. Older saves are migrated
in place.

- **Multi-race**: create races from templates (kart endurance, car endurance,
  sprint, motorcycle sprint, sim endurance, heats, blank), switch, delete.
- **Setup**: event, series, round, team, entry number, class, date, green flag;
  format and rules (timed or lap-count race, fixed stints / free strategy / no
  stops, minimum stops, min/max stint, drive-time limits, driver change and
  vehicle swap rules, pit lane loss, minimum pit time, radios, ballast);
  vehicle (discipline, make/model, fuel capacity and burn, tyre life and sets);
  track (name, location, lap length in km or mi, layout, direction, turns);
  conditions (forecast, air and track temperature, surface, wind, light);
  driver roster with weights, licences and ballast needs; a checklist with
  deadlines.
- **Strategy**: tap-to-assign stint plan in minutes or laps, per-stint lengths
  for free strategy, rule checks (consecutive stints, drive-time limits, stint
  bounds, fuel range, planned total vs race length), a stop calculator driven
  by fuel, tyres, and drive limits that builds an N-stop plan, targets, notes.
- **Sessions**: practice, qualifying, warm-up and heat sessions with per-driver
  lap logging, conditions, automatic best, grid position.
- **Race**: stint table (planned window, actual start, driver, vehicle number,
  positions, pit time, fuel, tyres, best lap, laps, notes), per-stint lap
  logger that accepts a lap time or per-sector splits, a stint countdown with
  pit-board or radio prompts, a lap stopwatch with a SECTOR button, a
  timestamped race log (flags, safety car, pit, penalty, incident, weather),
  and the result with finish position, fastest-lap and pole holder, debrief.
- **Map**: race-progress ring with proportional stint arcs, timing tower from
  rival positions, pit-window timeline, live clock and NOW cursor.
- **Rivals**: competitor entries with number, class, per-stint positions and
  finishing position, position-trace chart.
- **Analysis**: best/avg/consistency tiles, average speed from lap length,
  per-driver and per-stint tables, session-by-session best laps, a sector table
  (best sector per driver, ideal lap, time left on the table), lap-time chart.
- **Series**: championship standings across every race sharing a series name.
  Configurable points by position, fastest-lap and pole bonuses, drop-worst
  results, and manual adjustments for penalties or rounds held outside the app.

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
