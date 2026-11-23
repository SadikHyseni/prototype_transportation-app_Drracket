# Move-On: Transport Route Planner (DrRacket)

A prototype journey planner for a simplified London Underground network, built in Racket with a desktop GUI. Pick a starting station and a destination, and the app shows the route and an estimated journey time.

<img width="564" alt="Stations-Map" src="https://github.com/SadikHyseni/prototype_transportation-app_Drracket/assets/122787525/75e2a211-75a3-4940-b8c2-c7186f755040">

![App screenshot](https://github.com/SadikHyseni/prototype_transportation-app_Drracket/assets/122787525/aede83c1-2da6-4fee-9025-2211dae3c022)

## Features

- **Route planning** across two lines: Bakerloo and Metropolitan
- **Shortest direction**: the Metropolitan line is a loop, so the app picks the direction with fewer stops
- **Changing lines**: plans journeys that use both lines
- **Journey time** estimate in minutes
- **Accessibility info** for each station
- **Reverse** button to swap the start and destination
- **Clear** button to reset everything

## Stations

| Line | Stations |
|------|----------|
| Bakerloo | Harrow, Kenton, South Kenton, North Wembley, Wembley Central |
| Metropolitan | Northwick Park, Kenton, Baker Street, Euston Square, Wembley Central, Liverpool Street, Wembley Park |

Kenton and Wembley Central are on both lines, so you can change there.

### Accessibility Key

| Symbol | Meaning |
|--------|---------|
| (R) | Ramp access |
| (A) | Step-free access by lift |
| (T) | Toilets at the station |

## How It Works

- Each line is stored as a **graph** of connected stations, with links in both directions.
- A **path-finding** search checks whether the destination can be reached and builds the route.
- A **lookup table** of travel times between stations gives the estimated journey time.

## Requirements

- [DrRacket](https://racket-lang.org/) (Racket 8.x or later)

## How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/SadikHyseni/prototype_transportation-app_Drracket.git
   ```
2. Open `project_code` in DrRacket.
3. Click **Run**. The **Move-On** window opens.
4. Choose a **Location** and a **Destination**, then click **Get me there!**

## Built With

- Racket
- `racket/gui` for the desktop interface

## License

MIT License. See [LICENSE](LICENSE).
