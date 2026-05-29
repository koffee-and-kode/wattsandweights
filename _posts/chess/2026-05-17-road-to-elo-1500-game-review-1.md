---
title: "Road to ELO 1500 — Game Review #1"
date: 2026-05-17 11:00:00 +0530
tags: [chess, road-to-1500, game-review, stockfish]
excerpt: "50 rapid games this weekend — 26W/24L, net +12 rating. Stockfish says the endgame is where I'm bleeding."
---

First weekly game review. I exported the last 50 rapid games from chess.com and ran them through Stockfish (depth 12). The picture is clearer than I thought, and not in a flattering way.

## The week in numbers

50 rapid (10|0) games over May 15–17.

| | |
|---|---|
| W / L / D | **26 / 24 / 0** |
| Win rate | 52% |
| Rating arc | 759 → 771 (peak 821, low 749) |
| Avg ACPL | 65.7 |
| Blunders | 68 (1.36/game) |
| Mistakes | 154 |
| Inaccuracies | 178 |
| Lost on time | 2 |

The summary version: I beat people my level just about as often as they beat me, but neither side is playing clean chess. **1.36 blunders per game** means most games are decided by who blunders second.

## Where the leaks are: the endgame

Mistakes by phase (user moves only):

| Phase | Blunders | Mistakes | Inaccuracies |
|---|---:|---:|---:|
| Opening (moves 1–10) | 9 | 48 | 54 |
| Middlegame (11–25) | 25 | 76 | 79 |
| **Endgame (26+)** | **34** | 30 | 45 |

Half of all my blunders happen *after* move 25 — once queens are off and I actually have to find a plan. The opening is fine; the middlegame is the standard rating-bracket mess; the endgame is the single biggest leak.

## Opening repertoire — what's working, what isn't

Almost every game is 1.e4. As Black, I almost always answer 1...e5. The top positions after 6 plies:

| Position | Played | W | L |
|---|---:|---:|---:|
| Italian, 3.Bc4 Bc5 (Giuoco) | 5 | 3 | 2 |
| Scotch, 3.d4 exd4 | 4 | 1 | **3** |
| Two Knights, 3.Nc3 Nf6 | 4 | 3 | 1 |
| Italian, 3.Bc4 h6 | 3 | **3** | 0 |
| Italian, 3.Bc4 d6 | 2 | 2 | 0 |
| Nc3 Bb4 (Three Knights) | 2 | 0 | 2 |

The Italian / Giuoco lines (anything with 3.Bc4) — **8W/2L combined**. That's clearly the repertoire I should commit to.

The Scotch (3.d4 exd4) is bleeding — **1W/3L**. Either I drill those lines properly or I stop playing it and lock in 3.Bc4.

## Three blunders that show the pattern

**Game 15, move 24 — Re1?? (best Bxg7)**
+353cp → −71cp. Winning a clearly won game and I reach for a "developing" rook move instead of taking the bishop with check-followed-by-mate threats. I still won, because the opponent blundered worse. Lucky, not good.

**Game 22, move 12 — a4?? (best f4)**
Italian setup, around move 12 I went pawn-grabbing on the queenside while the centre was screaming for f4. Lost 311 cp and the game. Classic "I had a plan but it wasn't the position's plan."

**Game 11, move 10 — d5?? (best Kh7)**
Scotch as Black. Played a thematic-looking pawn push that actually walked into a forced sequence. The engine wanted a quiet king move; I wanted a "thinking-player move." The game was effectively lost on move 10.

## Worst games (highest ACPL)

| # | Opponent | Result | ACPL | Blunders / Mistakes |
|---:|---|---|---:|---:|
| 34 | IPlayChess2434 | won | 160 | 6 / 6 |
| 2 | Alienontour | lost | 143 | 4 / 9 |
| 15 | chessenjoyerguy | won | 124 | 5 / 1 |
| 47 | Tunderhino | won | 111 | 4 / 9 |
| 33 | Albee34 | won | 101 | 3 / 6 |

Three of my five sloppiest games this weekend were *wins*. That's the rating bracket — both sides are throwing pieces and someone has to be left holding the king.

## Historical context

I also ran the previous 50 games (a longer tail going back to late 2024). The patterns line up almost exactly:

- Win rate 42% (vs 52% recent) — slight recent uptick.
- Avg ACPL 65.6 — identical.
- Endgame blunders proportionally the same.
- Same opening repertoire, same Scotch problem.

Translation: the recent improvement is more "I'm playing more games" than "I've fixed anything." The leaks haven't moved.

## What's next (before Game Review #2)

Endgame is the leak. Italian is working. Plan for the week — about 90 minutes of study, plus four habit changes that cost zero extra time.

**Learn** (≈90 min total)

- **K+P vs K** — opposition, key squares, rule of the square. 30 min on the [Lichess endgame trainer](https://lichess.org/training/endgame).
- **Rook endings** — Lucena and Philidor positions, plus "rook behind the passer." 30 min: one Hanging Pawns video + 10 R+P vs R drills.
- **Lock the Italian** — drop the Scotch. Build a 3-move-deep response tree for 3.Bc4 lines using the Lichess opening explorer. 30 min, one-time.

**Do** (every game)

- **Switch to 15|10** rapid. Increment fixes endgame clock panic, which is half the leak.
- **Before every move: name the opponent's three best replies.** If I can only think of one, I haven't looked hard enough.
- **When ahead in material: trade pieces, push pawns.** Three of my five sloppiest games this week were wins where I kept the position complicated instead of simplifying.
- **Queens off the board → 10 seconds minimum per move.** My endgame moves currently take the same clock time as my opening moves. Backwards.

Targets for next week: blunders/game under 1.1, endgame blunder share under 40%, ACPL under 60. Back with Game Review #2.

---

*Generated with the `chess-game-review` skill — Stockfish 17, depth 12, [python-chess](https://python-chess.readthedocs.io/). Move classification thresholds: inaccuracy ≥ 50cp, mistake ≥ 100cp, blunder ≥ 300cp, per-move loss capped at 1000cp.*
