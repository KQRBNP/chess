stockfish

setoption name Debug Log File value <Filename>



uci <- getOptions


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
