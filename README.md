# ♟ Andoma

[![](https://github.com/healeycodes/andoma/workflows/Go/badge.svg)](https://github.com/healeycodes/andoma/actions?query=workflow%3AGo)

A chess engine called _Andoma_ (after its authors _Andrew_ and _Roma_).

It implements:
- Alpha-beta pruning for move searching
- Tomasz Michniewski's [Simplified Evaluation Function](https://www.chessprogramming.org/Simplified_Evaluation_Function) for board evaluation and piece-square tables
- A slice of the Universal Chess Interface (UCI) to allow challenges via lichess.org

<br>

An example interaction with the engine (responses are commented):

```bash
uci
# id name Andoma
# id author Andrew Healey & Roma Parramore
# uciok
position startpos moves e2e4
go
# bestmove h7h5
```

<br>

## Lichess.org

The UCI protocol slice that's implemented by this engine means you can play it via lichess.org by using [ShailChoksi/lichess-bot](https://github.com/ShailChoksi/lichess-bot) (a bridge between Lichess API and chess engines) and a BOT account.

<br>

## Development

Start the engine with:

`go run main.go`

Build with:

`go build`

<br>

## Tests

There are some unit tests you can run with:

`go test ./...`
