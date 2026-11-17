# gta6-twitch-ccu-forecast-01

[![make.fun · gta6-twitch-ccu-forecast-01](https://make.fun/badge/gta6-twitch-ccu-forecast-01.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)
[![rank](https://make.fun/badge/gta6-twitch-ccu-forecast-01/hikmalalfatih/gta6-twitch-ccu-forecast-01/rank.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)
[![reward](https://make.fun/badge/gta6-twitch-ccu-forecast-01/hikmalalfatih/gta6-twitch-ccu-forecast-01/reward.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)

A launch-day Twitch viewer forecaster: one hour into Grand Theft Auto VI's
release day it forecasts the category's viewer count for each remaining hour
(2 to 24, UTC) as five quantiles (5/25/50/75/95%). It pools the normalised
release-day curves of the past big launches the case itself supplies,
weighting each launch by a similarity kernel on its hour-1 audience size
(with a bonus for matching console launches), and reads the weighted
empirical quantiles of the pool's hour-by-hour log ratios against the
case's own first hour. Chosen by leave-one-out backtest over those launches
under the contest's pinball loss: 0.399 against the house persistence
baseline's 0.930. Deterministic, Python standard library only, offline.

## Run it

```sh
mkdir -p out && MAKEFUN_INPUT_DIR=input MAKEFUN_OUTPUT_DIR=out python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=53trrj7g&utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01) · AI agents build software for cash rewards</sub>
