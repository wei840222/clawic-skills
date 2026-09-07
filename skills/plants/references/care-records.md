# Plant Care Records

## Record layout

Keep one record per plant at `<state_root>/plants/<plant-name>.md`. Create it only after the user asks to save information.

```markdown
# <Common name>

- Scientific name: <confirmed name or unknown>
- Location: <location>
- Acquired: <YYYY-MM-DD or unknown>
- Light: <observed or recommended conditions>
- Watering cue: <soil-depth and condition check>
- Potting mix / drainage: <known details>

## Care log
- <YYYY-MM-DD>: <watering, fertilizer, repotting, symptom, or observation>
```

Record photos under `<state_root>/photos/<plant-name>/` only when the user has chosen to retain them; link each image from the plant record with date and context. Keep optional seasonal planning in `<state_root>/care-calendar.md`, shopping items in `<state_root>/wishlist.md`, and propagation attempts in the parent plant's record.

## Care routines

- **Watering:** Log date, method, soil condition, and visible response. Check the plant's defined soil-depth cue before watering; change the cue only when observations support it.
- **Fertilizing:** Log product and dilution. During active growth, follow the product label and plant-specific guidance; pause or reduce when growth and light decrease.
- **Repotting:** Log date, pot size, substrate, drainage, and root condition. Consider repotting when roots circle densely, drainage has degraded, or the plant repeatedly dries unusually quickly.
- **Propagation:** Log parent plant, date, method, medium, and progress until established.

## Reminder and history rules

Group care by observed needs only when that reduces work without erasing plant-specific cues. A reminder is a prompt to inspect, not an instruction to water automatically. If a plant is removed or dies, move its record to `<state_root>/archive/` and retain the known cause, attempts, and lessons. Never turn a plant loss into blame.
