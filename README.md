# tzwars

Daylight vs. the clock — a single-file, dependency-free visualization of the timezone wars.

Every row of the map is one day of the year; left to right is your local clock time,
shaded by real solar altitude (day, civil/nautical/astronomical twilight, night).
Drag the green block to your working hours, then compare how each clock policy —
permanent standard time, permanent DST, or seasonal switching (US/EU/AU rules) —
treats your year: dark starts, dark ends, and how much of your work time falls in daylight.

## Usage

Open `index.html` in a browser. That's it — no build, no server, no network.

- Pick a city preset, enter coordinates, or use browser geolocation.
- Drag the work block to move it, drag its edges to resize, or nudge with arrow keys
  (Shift = 1 hour steps).
- Hover the map for per-day sunrise/sunset and day length.
- Click a scoreboard row to switch DST policy.
- Settings live in the URL fragment — copy the address to share a configuration.

## How it works

Sunrise, sunset, and solar altitude are computed locally with the NOAA solar equations
(accurate to about a minute), including polar day/night handling. Seasonal DST policies
appear as the one-hour jumps in the daylight bands.
