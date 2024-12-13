<h1 style="text-align: center;">CellViz</h1>

[![GitHub release](https://img.shields.io/github/v/release/velocitatem/CellViz)](https://github.com/velocitatem/CellViz/releases) [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT) [![Build Status](https://img.shields.io/github/actions/workflow/status/velocitatem/CellViz/ci.yml)](https://github.com/velocitatem/CellViz/actions) [![Language: C++](https://img.shields.io/badge/language-C%2B%2B-%23f34b7d)](https://en.wikipedia.org/wiki/C%2B%2B) [![Platform: Ubuntu](https://img.shields.io/badge/platform-Ubuntu-orange)](https://ubuntu.com/) [![Platform: WSL](https://img.shields.io/badge/platform-Windows-blue)](https://learn.microsoft.com/en-us/windows/wsl/install)

Cellular Automata inspired by live-data visualization, designed to handle multidimensional and high-throughput data efficiently.

<div style="text-align: center;">
  <img src="https://github.com/user-attachments/assets/5206dec2-d7c7-43cb-b913-4b2c32efb07d" alt="Output Image">
</div>

## Requirements

- Find more about the project here : [Documentation](https://velocitatem.github.io/CellViz/)

  
## Authors
![Contributors](https://contrib.rocks/image?repo=velocitatem/CellViz)

## Requirements

To build and run CellViz, you will need:

- Boost dev libraries (not runtime)
- JsonCpp dev libraries
- Nlohmann Json dev libraries
- CMake
- SFML
- Alpha Vantage API Key

### Installation on Ubuntu

```bash
sudo apt-get update && sudo apt-get install -y cmake g++ lcov libboost-all-dev libsfml-dev libgtest-dev nlohmann-json3-dev libcurl4-openssl-dev libgtk-3-dev libjsoncpp-dev
```

To use the Alpha Vantage API key, set the environment variable:

```bash
export API_KEY=YOUR_ALPHA_VANTAGE_KEY
```

## Project Structure

```mermaid
sequenceDiagram
    participant User
    participant Main
    participant Board
    participant SmithLife

    User->>Main: Start Application
    Main->>Board: Create Board(Z, Z)
    Main->>CellularLife: Create life cells
    Main->>Board: Add life cells
    loop Update Board
        Main->>CellularLife: Call compute()
        CellularLife->>Board: Update grid
        Board->>Main: Render board
    end
```

## Features

- Visualizes cellular automata for high-throughput, multidimensional data.
- Implements live-data feeds with Alpha Vantage integration.
- Built with C++ and optimized for performance.
- Modular architecture for easy addition of new data types.

## Getting Started

Clone the repository:

```bash
git clone https://github.com/velocitatem/CellViz.git
```

Navigate to the project directory:

```bash
cd CellViz
```

Build the project using CMake:

```bash
mkdir build && cd build
cmake ..
make
```

Run the application:

```bash
./CellViz
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
