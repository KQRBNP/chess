Inspirational:

https://deepmind.com/research/publications/Mastering-Atari-Go-Chess-and-Shogi-by-Planning-with-a-Learned-Model

The brain is the best example of a general reinforcement learning algo.

<a href="https://en.wikipedia.org/wiki/Demis_Hassabis">Demis Hassabis</a> has a PhD in neuroscience and sought to connect brain and machine learning: DeepMind's mission is to "solve intelligence" and then use intelligence "to solve everything else". Connecting psychology with intelligence and thus artificial intelligence to help solve the world's problems.

<a href="https://towardsdatascience.com/deepmind-unveils-muzero-a-new-agent-that-mastered-chess-shogi-atari-and-go-without-knowing-the-d755dc80ff08">MuZero</a>: "At every one of these steps the model predicts the policy (e.g. the move to play), value function (e.g. the predicted winner), and immediate reward (e.g. the points scored by playing a move)"

---

Alpha Zero

https://deepmind.com/blog/article/alphazero-shedding-new-light-grand-games-chess-shogi-and-go

"AlphaZero replaces the handcrafted knowledge and domain-specific augmentations used in
traditional game-playing programs with deep neural networks, a general-purpose reinforcement
learning algorithm, and a general-purpose tree search algorithm."

https://www.youtube.com/watch?v=MPXGiowUr0o

https://medium.com/applied-data-science/how-to-build-your-own-alphazero-ai-using-python-and-keras-7f664945c188

---

stockfish

setoption name Debug Log File value <Filename>



uci <- Information about available options.
```
uci
id name Stockfish 11 64 BMI2
id author T. Romstad, M. Costalba, J. Kiiski, G. Linscott

option name Debug Log File type string default 
option name Contempt type spin default 24 min -100 max 100
option name Analysis Contempt type combo default Both var Off var White var Black var Both
option name Threads type spin default 1 min 1 max 512
option name Hash type spin default 16 min 1 max 131072
option name Clear Hash type button
option name Ponder type check default false
option name MultiPV type spin default 1 min 1 max 500
option name Skill Level type spin default 20 min 0 max 20
option name Move Overhead type spin default 30 min 0 max 5000
option name Minimum Thinking Time type spin default 20 min 0 max 5000
option name Slow Mover type spin default 84 min 10 max 1000
option name nodestime type spin default 0 min 0 max 10000
option name UCI_Chess960 type check default false
option name UCI_AnalyseMode type check default false
option name UCI_LimitStrength type check default false
option name UCI_Elo type spin default 1350 min 1350 max 2850
option name SyzygyPath type string default <empty>
option name SyzygyProbeDepth type spin default 1 min 1 max 100
option name Syzygy50MoveRule type check default true
option name SyzygyProbeLimit type spin default 7 min 0 max 7
```


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
setoption name Clear Hash
setoption name Threads value 8
setoption name Hash value 8192
setoption name SyzygyPath value /Users/daniel/My-Files/My-R-projects/R-Chess/syzygy
go depth 20
```

```
position startpos moves e2e4 e7e6 d2d4 d7d5 e4e5 c7c5 c2c3 b8c6 g1f3 g8e7 f1d3 e7f5 d3c2 c5d4 c3d4 d8b6 c2f5 e6f5 e1g1 f8e7 b1c3 c8e6 h2h3 e8g8 a1b1 a8c8 c1f4 h7h6 f1e1 a7a6 a2a3 b6d8 f4d2 g7g5 b2b4 b7b5 c3e2 f5f4 b1b3 e6f5 b3c3 d8b6 d1a1 a6a5 b4a5 c6a5 c3c8 f8c8 e2c3 f5e6 a1b1 a5c4 c3b5 c8a8 d2b4 e7b4 b1b4 c4a3 e1a1 a8b8 b4a3 b6b5 f3h2 b5b4 a3a7 g8g7 h2g4 b8b7 a7a4 b4a4 a1a4 b7b1 g1h2 b1b2 h2g1 b2c2 a4a1 e6g4 h3g4 c2c4 a1d1 g7g6 g1f1 h6h5 g4h5 g6h5 f1e2 c4b4 e2d3 b4b3 d3c2 b3a3 c2b2 a3a8 b2c3 h5g6 d1d2 g6f5 d2b2 a8a3 c3b4 a3a1 b4c5 a1a5 c5b4 a5a6 b4b5 a6a8 b5c5 a8a5 c5b6 a5a3 b6c5
```

```
position fen rnbq1bn1/1p2kpp1/2Q1p2r/p1ppP2p/3P2P1/2P5/PP3P1P/RNB1KBNR b KQ - 1 8
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

put all files in the same folder

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
