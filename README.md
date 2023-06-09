# MazeSolver
[![LICENSE](https://img.shields.io/github/license/KThankYou/MazeSolver?color=blue)](LICENSE) ![Language](https://img.shields.io/badge/Language-C%2B%2B-brightgreen) ![Qt](https://img.shields.io/badge/Qt-6.5.0-brightgreen) ![GitHub csize](https://img.shields.io/github/languages/code-size/KThankYou/MazeSolver)

## Description

MazeSolver is a GUI application built with the Qt framework. It allows users to create and solve grids or mazes of their desired dimensions. The application provides an intuitive interface for creating, modifying, and solving mazes. It will find the shortest path to one of the the finish points from the start point.

## Installation

Download Release.7z from releases and extract the contents to a folder. Then run MazeSolver.exe.

## Building From Source

### Prerequisites

To build Maze Solver, you require the following on your system:

- C++17 or above
- Qt framework 6.5.0+
- Qt Creator Community 10.0.0+ 

### Cloning 

Open a command line in your desired folder, clone the repo and change the directory to the cloned folder using
```
git clone https://github.com/KThankYou/MazeSolver.git
cd MazeSolver
```

### Building
1. Open Qt Creator and load the project.
2. Switch to release and then build the project.
3. Copy the release exe from the build folder to your desired folder.
4. Open a command line in your bin folder in the Qt installation, ex: `"D:\Qt\6.5.0\mingw_64\bin"`
5. Use the `set PATH=<path_to_qt>;%PATH%` to use the Qt DLLs, ex:`set PATH=D:\Qt\Tools\mingw1120_64\bin;%PATH%`
6. Now run the `windeployqt6 "<path_to_exe>"` command to copy necessary DLLs to the exe folder, ex: `windeployqt6 "D:\MazeSolver\MazeSolver.exe"`

## Usage

1. Launch MazeSolver.exe
2. Choose LOAD to load a saved maze or enter a height and width and press START
3. Left click on the grids to toggle walls
4. Right click to open the context menu to get options to toggle starting position and ending position. There can only be a single start but multiple finish points can exist. It will find the nearest finish point.
5. Go to Menu and click Start to solve the maze.

#### Note:
- Menu->Save to save the current maze layout in a file. A layout can be created manually using a text editor.
- Menu->Reload to reload a layout if it was loaded from a file.
- Menu->Reset to get a blank canvas.
- Minimum Height is 3x3. Recommended maximum height is 68x98, going above which might crash the program.
- There is an example.txt file with a maze.
- In the saved layout: 
- - The first line is height and width separated by a white space
- - "W" represents walls, "S" represent the start point, "E" represents finish/end point, "." represents empty paths.

## License

This project is licensed under [The Unlicense](LICENSE).
