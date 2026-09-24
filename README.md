# TrapBook ♞

[![Stars](https://img.shields.io/github/stars/TitisBuyutKusumo/trapbook?style=social)](https://github.com/TitisBuyutKusumo/trapbook/stargazers)
[![Release](https://img.shields.io/github/v/release/TitisBuyutKusumo/trapbook)](https://github.com/TitisBuyutKusumo/trapbook/releases)
[![License](https://img.shields.io/github/license/TitisBuyutKusumo/trapbook)](LICENSE)

Free polyglot chess opening book loaded with traps. **3.8 MB · 247,907 positions · 64 trap lines · both colors.**

Your engine plays normal, respectable chess… until the opponent gets greedy. Then the book bites.

## What's inside

64 hand-built trap lines sitting on a full sound repertoire:

- **Mate in the opening** — Scholar's, Fool's, Legal's Mate, Opera trap
- **The famous gambit traps** — Stafford, Fried Liver, Evans, Möller, Cochrane
- **Two Knights chaos** — Traxler (both), Fritz, Ulvestad, Lolli, Nakhmanson, Blackburne Shilling
- **Ruy Lopez crimes** — Noah's Ark (traps the bishop!), Fishing Pole, Mortimer ideas
- **Sicilian punishments** — Siberian, Smith-Morra, Scotch, Göring, Grand Prix
- **Queen's Gambit traps** — Elephant, Rubinstein, Cambridge Springs, Winawer Countergambit
- **Gambit mayhem** — Budapest (Kieninger!), Englund, Albin-style lines, Danish, From's, Orangutan, Grob

Underneath: 107k theory positions + 8,731 attacking master games (Tal, Fischer, Kasparov, Marshall, Blackburne, Anderssen, Morphy, Chigorin). Trap moves are weighted to dominate, sound theory fills the rest.

## Who is this for

**Engine vs human — not engine vs engine.** Real test results:

| Matchup | Score |
|---|---|
| Stockfish + book vs Stockfish, no book (20 games) | 8.5/20 (−53 Elo, not significant) |
| Stockfish + book vs Maia 1600 | 8–0 |
| Stockfish + book vs blunder-prone play | 10–0 |

Translation: dubious gambits get refuted by perfect calculation, but humans grab the bait every time. If you want a tournament book for engine-vs-engine, this isn't it. If you want to farm humans, welcome home.

## Use it in 1 minute

**DroidFish (Android):** copy `booktrick.bin` to the `DroidFish/book` folder → menu → Select opening book. Done.

**Arena / Banksia / CuteChess / Scid vs. PC / Lucas Chess:** point the opening book path at the `.bin`. Done.

**Komodo, Rodent, Chess System Tal:** set the Book File option to the `.bin`. Done.

**Stockfish:** no native book support — use the [PolyGlot adapter](https://www.chessprogramming.org/PolyGlot) (plays book moves on the engine's behalf) or let your GUI apply the book.

Not for ChessBase/Fritz (proprietary `.ctg` only).

## Taste of the action

Scholar's Mate, served straight from the book:

```
1. e4 e5 2. Qh5 Nc6 3. Bc4 Nf6?? 4. Qxf7#
```

Stafford Gambit — Black "hangs" the queen, then mates:

```
1. e4 e5 2. Nf3 Nf6 3. Nxe5 Nc6 4. Nxc6 dxc6 5. d3 Bc5
6. Bg5 Nxe4 7. Bxd8 Bxf2+ 8. Ke2 Bg4#
```

More full games in [`demos/`](demos/) — every trapper move tagged `[book]` or `[engine]` so you can see exactly where the book did it.

## FAQ

**Will this make my engine stronger?**
No. A book steers the opening; it doesn't add Elo vs equal opposition. It makes your engine *more dangerous vs humans*.

**Why didn't the trap fire in my game?**
Traps need the victim to cooperate (greedy/wrong moves). Against correct play the engine just plays sound theory from the same book. That's by design — see "Who is this for" above.

**What format is this?**
Standard polyglot `.bin` (sorted, binary-search safe). Anything that reads polyglot books can use it.

## License

MIT — do whatever you want with it. See [LICENSE](LICENSE).
