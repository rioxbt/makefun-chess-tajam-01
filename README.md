# makefun-chess-tajam-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/rioxbt/makefun-chess-tajam-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/rioxbt/makefun-chess-tajam-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

`main.py` is the whole engine, at most 4,096 bytes: a 0x88 mailbox position
with make/unmake, a negamax search (principal variation search, iterative
deepening under a fixed node budget, transposition table used for move
ordering, killer moves, history heuristic, MVV-LVA, null move, late move
reductions, check extensions), a quiescence search over captures,
promotions and check evasions, and a tapered PeSTO middle/endgame
evaluation. Nothing reads a clock, so every position always gets the same
move and a replay comes out identical.

## Run it

```sh
node cli/makefun.mjs grade-local --kit <unpacked kit> --bot . --driver docker
```

---

<sub>Entered on [make.fun](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
