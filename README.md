# Stafford

Finds the chess mistakes you keep repeating across your recent chess.com games, ranks them by how many points they cost you, and turns each one into a practice puzzle from your own games.

Everything runs in the browser. Stockfish 10 (asm.js build, GPLv3) does the analysis. No server, no keys.

## Run it

Push this folder to a GitHub repo, then Settings > Pages > Deploy from branch > `main` / root.
It pulls games straight from the public chess.com API, so you just type a username.

Local test: `python3 -m http.server` in this folder, then open http://localhost:8000
(opening index.html as a file won't work, the engine needs to load as a worker over http).

## Files

- `index.html` the whole app
- `stockfish.js` the engine (loaded as a Web Worker)

Pieces: cburnett (CC BY-SA 3.0), embedded in index.html.
