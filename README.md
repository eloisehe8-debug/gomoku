# Gomoku

A Gomoku (five in a row) game that runs in the browser. Single HTML file, no dependencies.

**Play online:** https://eloisehe8-debug.github.io/gomoku/

Or open `index.html` locally.

## Features
- 1 Player: play against a bot, with Easy / Medium / Hard difficulty
- 2 Players: black vs. white on the same device
- Online: create a room and send the link to a friend; you play black on your computer, they play white on theirs
- 15 × 15 board
- Win detection in all four directions, with the winning line highlighted
- Undo (button or ⌘/Ctrl+Z), restart, and a running score saved in the browser
- Editable player names; the loser moves first in the next game
- English and Chinese interface (toggle in the top-right corner)
- Works on phones and in dark mode

## How online play works
Online games relay moves through a free public MQTT broker over secure WebSockets (HiveMQ, with EMQX as a fallback). Nothing is stored and no account is needed. Moves are not private: anyone who knows the room code could read them.
