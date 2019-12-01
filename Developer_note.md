stockfish

setoption name Debug Log File value <Filename>



uci <- getOptions

use stockfish interactively:

```
d

 +---+---+---+---+---+---+---+---+
 | r | n | b | q | k | b | n | r |
 +---+---+---+---+---+---+---+---+
 | p | p | p | p | p | p | p | p |
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   |
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   |
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   |
 +---+---+---+---+---+---+---+---+
 |   |   |   |   |   |   |   |   |
 +---+---+---+---+---+---+---+---+
 | P | P | P | P | P | P | P | P |
 +---+---+---+---+---+---+---+---+
 | R | N | B | Q | K | B | N | R |
 +---+---+---+---+---+---+---+---+

Fen: rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1
Key: B4D30CD15A43432D
Checkers: 

eval

     Term    |    White    |    Black    |    Total   
             |   MG    EG  |   MG    EG  |   MG    EG 
 ------------+-------------+-------------+------------
    Material |  ----  ---- |  ----  ---- |  0.00  0.00
   Imbalance |  ----  ---- |  ----  ---- |  0.00  0.00
  Initiative |  ----  ---- |  ----  ---- |  0.00  0.00
       Pawns |  0.35 -0.08 |  0.35 -0.08 |  0.00  0.00
     Knights |  0.01 -0.17 |  0.01 -0.17 |  0.00  0.00
     Bishops | -0.05 -0.41 | -0.05 -0.41 |  0.00  0.00
       Rooks | -0.37 -0.02 | -0.37 -0.02 |  0.00  0.00
      Queens |  0.00  0.00 |  0.00  0.00 |  0.00  0.00
    Mobility | -0.94 -1.10 | -0.94 -1.10 |  0.00  0.00
 King safety |  0.72 -0.08 |  0.72 -0.08 |  0.00  0.00
     Threats |  0.00  0.00 |  0.00  0.00 |  0.00  0.00
      Passed |  0.00  0.00 |  0.00  0.00 |  0.00  0.00
       Space |  0.62  0.00 |  0.62  0.00 |  0.00  0.00
 ------------+-------------+-------------+------------
       Total |  ----  ---- |  ----  ---- |  0.00  0.00

Total evaluation: 0.10 (white side)
```

```
setoption name SyzygyPath value /Users/daniel/My-Files/My-R-projects/R-Chess/syzygy
setoption name Threads value 8
setoption name Hash value 8192
setoption name ponder value true
go depth 15
```

-------


compile stockfish

https://github.com/official-stockfish/Stockfish

make build ARCH=x86-64-bmi2


-------

Universal Chess Interface (UCI) engine protocol

https://www.shredderchess.com/download.html

Use UCI:

https://stackoverflow.com/questions/17003561/using-the-universal-chess-interface

```
go
info depth 1 seldepth 1 multipv 1 score cp 116 nodes 20 nps 20000 tbhits 0 time 1 pv e2e4
info depth 2 seldepth 2 multipv 1 score cp 112 nodes 54 nps 54000 tbhits 0 time 1 pv e2e4 b7b6
info depth 3 seldepth 3 multipv 1 score cp 148 nodes 136 nps 136000 tbhits 0 time 1 pv d2d4 d7d6 e2e4
info depth 4 seldepth 4 multipv 1 score cp 137 nodes 247 nps 123500 tbhits 0 time 2 pv d2d4 e7e6 e2e4 c7c6
info depth 5 seldepth 5 multipv 1 score cp 77 nodes 1157 nps 385666 tbhits 0 time 3 pv c2c3 d7d5 d2d4 b8c6 c1g5
info depth 6 seldepth 6 multipv 1 score cp 83 nodes 2250 nps 562500 tbhits 0 time 4 pv e2e4 b8c6 d2d4 d7d6 f1c4 g8f6
info depth 7 seldepth 7 multipv 1 score cp 67 nodes 4481 nps 640142 tbhits 0 time 7 pv e2e4 e7e5 d2d4 e5d4 d1d4 b8c6 d4d1
info depth 8 seldepth 8 multipv 1 score cp 60 nodes 7849 nps 872111 tbhits 0 time 9 pv e2e4 e7e5 g1f3 d7d5 d2d4 b8c6 f3e5
info depth 9 seldepth 8 multipv 1 score cp 60 nodes 11187 nps 932250 tbhits 0 time 12 pv e2e4 e7e5 g1f3 d7d5 d2d4 b8c6 f3e5
bestmove e2e4 ponder e7e5
```

info | ply search depth | <a href="https://www.chessprogramming.org/Depth#Selective_Search_Depth">Selective Search Depth</a>  | multi <a href="https://www.chessprogramming.org/Principal_Variation">PV</a> | score | nodes Searched | <a href="https://www.chessprogramming.org/Nodes_per_Second">Nodes Per Second</a> | TableBase Hits | time elapsed (ms) | <a href="https://www.chessprogramming.org/Principal_Variation">PV</a> Line
--- | --- | --- | --- | --- | --- | --- | --- | --- | ---
info | depth 1 | seldepth 1 | multipv 1 | score <a href="https://chess.fandom.com/wiki/Centipawn">cp</a> 116 | nodes 20 | nps 20000 | tbhits 0 | time 1 | pv e2e4


-------

option name Hash type spin default 16 min 1 max 131072

131072 --> 131072 MB --> 131.072 GB (spin's unit)

8192 MB

16000 -> 16 GB

-------

https://github.com/official-stockfish/Stockfish/blob/master/Readme.md

https://lichess.org/

Source Code: https://lichess.org/source

----

Smallfish-related: 
https://github.com/fsmosca/chess-artist

----

Endgame table
https://github.com/niklasf/syzygy-tables.info

wget -e robots=off --reject="index.html*" --quiet --no-parent --recursive --relative --no-directories http://tablebase.sesse.net/syzygy/3-4-5/

WDL (win/draw/loss) and DTZ (distance to zero)

---

Evaluation:

https://github.com/hxim

https://github.com/niklasf/stockfish.js/

https://www.chessprogramming.org/Evaluation

https://hxim.github.io/Stockfish-Evaluation-Guide/

---

https://chess.fandom.com/wiki/Centipawn

https://python-chess.readthedocs.io/en/latest/index.html
