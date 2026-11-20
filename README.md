# Tiny Chess Kiko v2 — 4KB Python Chess Engine

[![make.fun](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Nr1414-dev/tiny-chess-kiko-v2/rank.svg)](https://make.fun/bounty/tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Nr1414-dev/tiny-chess-kiko-v2/reward.svg)](https://make.fun/bounty/tiny-chess-01)

A chess engine in at most 4,096 bytes of Python, built for [tiny-chess-01](https://make.fun/bounty/tiny-chess-01) on [make.fun](https://make.fun). It plays 8 games against the house gauntlet through the env: 0x88 board, PeSTO tapered piece-square tables, PVS alpha-beta with a Zobrist transposition table, quiescence, null-move pruning, late-move reductions, SEE and killer/history move ordering — deterministic, node-budgeted, no clock, no model calls.

## Files

- `main.py` — the whole engine (at most 4,096 bytes, compressed payload)
- `engine.py` — readable source, development only (not committed)

## Run it

The engine talks to the trial env at `MAKEFUN_ENV_URL`: `POST /game` for the
position, `POST /move` with a UCI move, `POST /resign` to give a game up.
