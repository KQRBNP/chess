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

-------


compile stockfish

https://github.com/official-stockfish/Stockfish

make build ARCH=x86-64-bmi2


-------

Universal Chess Interface (UCI) engine protocol

https://www.shredderchess.com/download.html


-------

option name Hash type spin default 16 min 1 max 131072

131072 --> 131072 MB (spin's unit)

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

---

Evaluation:

https://github.com/hxim

https://github.com/niklasf/stockfish.js/

https://www.chessprogramming.org/Evaluation

https://hxim.github.io/Stockfish-Evaluation-Guide/

---

https://chess.fandom.com/wiki/Centipawn
