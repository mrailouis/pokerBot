<h1 align="center">
  PokerBot
</h1>

<div align="center">
  <b>A local terminal assistant for Texas Hold'em-style poker sessions</b><br>
  <sub>Simple, lightweight, and built for pass-and-play games</sub>
</div>

<br>

<div align="center">

[![Made with Python](https://img.shields.io/badge/Made%20With-Python%203-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Project Status](https://img.shields.io/badge/Status-Archived-6B7280?style=for-the-badge)](#project-status)
[![License](https://img.shields.io/github/license/mrailouis/pokerBot?style=for-the-badge&color=blue)](LICENSE)

</div>

---

## What is PokerBot?

**PokerBot** is an archived Python terminal application for setting up a local poker table. It registers players, prepares a standard 52-card deck, assigns private cards, creates an opening flop, and displays each player's hand and starting balance in sequence.

The project was designed for **local pass-and-play sessions** where players share one terminal. It focuses on table setup and card dealing rather than managing a complete game.

---

## Features

<details>
<summary><b>Player Setup</b></summary>
<br>
Creates a table from names entered at the start of the session.

- Prompts for the number of players
- Records a name for each seat
- Keeps player cards and balances together for the session
</details>

<details>
<summary><b>Shared Deck Dealing</b></summary>
<br>
Draws cards from one standard 52-card deck.

- Prepares a three-card flop
- Assigns two private cards to every player
- Removes drawn cards from the deck to avoid duplicates
</details>

<details>
<summary><b>Pass-and-Play Hand Display</b></summary>
<br>
Reveals one player's cards at a time so the terminal can be passed around the table.

- Displays the current player's private cards
- Waits before advancing to the next player
- Clears the terminal between players
</details>

<details>
<summary><b>Starting Balances</b></summary>
<br>
Applies one starting balance to the full table and shows it beside each hand.

- Uses the same opening amount for every player
- Keeps a separate balance entry for each player
- Provides a balance field that could support betting later
</details>

<details>
<summary><b>Terminal Presentation</b></summary>
<br>
Provides a simple local interface for the session.

- Animated "Louis' Poker House" introduction
- ANSI-styled card and balance output
- Console clearing on Windows, macOS, and Linux
</details>

---

## Getting Started

### Requirements

- Python 3
- Git
- A local desktop terminal with ANSI color support

### macOS and Linux

```bash
git clone https://github.com/mrailouis/pokerBot.git
cd pokerBot
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install pyautogui
python3 main.py
```

### Windows

```powershell
git clone https://github.com/mrailouis/pokerBot.git
cd pokerBot
py -m venv .venv
.venv\Scripts\activate
py -m pip install pyautogui
py main.py
```

The current prototype imports `pyautogui`, so it must be installed even though the game flow does not use desktop automation yet.

---

## How It Works

1. Enter the number of players and a name for each player.
2. PokerBot prepares the deck, reserves the flop, and deals two private cards per player.
3. Enter the starting balance that should be assigned to the table.
4. Pass the terminal between players to reveal each hand privately.

The application is interactive and should be run from a terminal rather than imported as a library.

---

## Project Structure

| File | Purpose |
| --- | --- |
| `main.py` | Starts the application and coordinates balances and hand display |
| `playerCount.py` | Collects player count and names |
| `flop.py` | Creates the deck and prepares the opening flop |
| `cardAssign.py` | Deals two private cards to each player |
| `animation.py` | Displays the terminal welcome animation |
| `clearConsoleCMD.py` | Clears the terminal for the active operating system |

---

## Project Status

PokerBot is **archived** and no longer actively maintained. It is kept here as a historical snapshot of an early learning project.

The version in this repository demonstrates player registration, card assignment, starting balances, and sequential hand display. It is not a complete poker engine.

The following parts were never implemented:

- Betting rounds and balance updates
- Small-blind and big-blind rotation
- Flop display, turn, and river progression
- Hand evaluation and winner selection
- Showdown and pot distribution
- Full input validation and recovery from invalid entries

The prototype's dealing and blind-selection paths still have rough edges, including an occasional deck index error while preparing the flop.

---

## License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## Credits

<table>
  <tr>
    <td align="center"><a href="https://github.com/mrailouis"><b>Louis-LLC</b></a><br><sub>Original creator</sub></td>
  </tr>
</table>

---

<div align="center">
  <sub>Archived project — built for local poker nights.</sub>
</div>
