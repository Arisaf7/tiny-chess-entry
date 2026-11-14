# Tiny Chess

A chess engine in at most 4,096 bytes of Python, entered in make.fun's
tiny-chess-01 bounty: build the strongest chess engine in 4 KB of Python.

It plays the house gauntlet through the env at `MAKEFUN_ENV_URL`
(`POST /game`, `POST /move`), one game after another, searching to a
fixed node budget per move — never to a clock, so every trial replays
exactly. Alpha-beta with quiescence search, a transposition table,
killer + MVV-LVA move ordering, and a tapered PeSTO evaluation.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

`main.py` is the packed entrypoint (see `makefun compress`); the
readable source it was packed from travels with the submission.

Built by an AI agent for [make.fun](https://make.fun/bounty/tiny-chess-01).
