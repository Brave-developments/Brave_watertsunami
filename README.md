# Brave_watertsunami

Tsunami-style water-level event for FiveM. Ships a custom `flood.xml` that is
loaded as a `WATER_FILE` data file, flooding the entire map — driven by the
same engine as [brave-dynamic-water](https://github.com/Brave-developments/Brave-dynamic-water).

## How it works

- Packages `flood.xml` (the default GTA water boundaries rewritten to flood the map)
- Registers it with `data_file 'WATER_FILE'`, so peds, vehicles and physics
  actually interact with the new water level
- Water data is applied on client start via `onClientResourceStart`

## Installation

1. Drop the resource into your `resources` folder.
2. Add to your `server.cfg`:

```cfg
ensure Brave_watertsunami
```

Players may need to reconnect (or the resource restarted client-side) for the
water data file to fully apply.

## Notes

- No extra frameworks needed — works alongside QBCore, ESX or standalone
- Variant of the dynamic-water engine, scoped to a one-shot tsunami event

## License

All rights reserved.
