# Super Tic Tac Toe

Second iteration of the Ultimate Tic Tac Toe project, implemented in C++17. The overall application is multi-threaded to support graphics rendering, user input, and game loop concurrently, while the AI bot logic itself runs on a single dedicated thread.

> Forked from [CzmeleN/SuperTicTacToe](https://github.com/CzmeleN/SuperTicTacToe).

## Overview

This repository contains **Version 2** of my Ultimate Tic Tac Toe bot:

- **Version 1**:
  - Language & Concurrency: C with multi-threading for both UI and bot simulations.
  - Bot algorithm: Monte Carlo Tree Search only.
  - Repositories:
    - Full project: [Super_tictactoe_SDL](https://github.com/Hinski2/Super_tictactoe_SDL)
    - Bot-focused: [bot_utlimate_tic_tac_toe](https://github.com/Hinski2/bot_utlimate_tic_tac_toe)
  - Performance report: [raport_ze_stanu_bota_9x9.md](https://github.com/Hinski2/bot_utlimate_tic_tac_toe/blob/main/raport_ze_stanu_bota_9x9.md)

- **Version 2 (this repo)**:
  - Language & Concurrency: C++17 with multi-threaded application (UI, rendering, input) and a single-threaded AI engine for consistent benchmarking.
  - Bot algorithms:
    - **Random Bot**
    - **MCS Bot** (flat mc)
    - **Minimax Bot** (α‑β pruning)
    - **MCTS Bot** (UCT selection)
  - Performance analysis: [botPerfomenceAnalys.md](botPerfomenceAnalys.md)

## Features

- **AI Difficulty Modes**: Easy / Medium / Hard settings across all agents.
- **Modular Codebase**:
  - `engine/` – game rules and logic
  - `src/`    – application entry and game loop
  - `include/`– header files
  - `utils/`  – helper functions and data handling
  - `tests/`  – unit tests
  - `assets/` – textures and UI resources
- **Performance Logging**: Detailed FPS and bot move-time logs for benchmarking.

## Bot Performance Summary

- **Version 1 Report**: In-depth stats on Monte Carlo performance and win rates over multiple thread counts ([raport_ze_stanu_bota_9x9.md](https://github.com/Hinski2/bot_utlimate_tic_tac_toe/blob/main/raport_ze_stanu_bota_9x9.md)).
- **Version 2 Highlights**: Multiple algorithms tested on 9×9 boards; MCS Bot outperforms others in win ratio, while MCTS offers best exploration–exploitation balance (see [botPerfomenceAnalys.md](botPerfomenceAnalys.md)).

## Build & Run

```bash
git clone https://github.com/Hinski2/SuperTicTacToe.git
cd SuperTicTacToe
make                # builds the application
./SuperTicTacToe    # launches the GUI with bot vs. bot or human vs. bot
```

## Comparison with Version 1

| Aspect                | Version 1 (C + Multi-threaded Bot & UI)                                     | Version 2 (C++17 + Multi-threaded App, Single-threaded Bot)       |
|-----------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------|
| Repository            | [Super_tictactoe_SDL](https://github.com/Hinski2/Super_tictactoe_SDL)        | This repository                                                  |
| AI Algorithms         | MCTS only                                                                    | Random, MCS, Minimax, MCTS                                       |
| Concurrency           | Bot and UI both multi-threaded                                               | UI, rendering, input multi-threaded; AI engine single-threaded    |
| Performance Report    | [9×9 MCTS report](https://github.com/Hinski2/bot_utlimate_tic_tac_toe/blob/main/raport_ze_stanu_bota_9x9.md) | [Multi-algo analysis](botPerfomenceAnalys.md)                    |
| Language              | C                                                                            | C++17                                                             |

## Contributing

Contributions, issues, and feature requests are welcome. Please open an issue or submit a pull request.

## License

Distributed under the MIT License. See [LICENSE](LICENSE) for details.

