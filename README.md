# CommandLineGame

A C++ terminal game made for my first-year university coursework.
Choose a Wizard, Warrior, Assasin, or Archer, fight monsters in dungeons, and buy equipment from the shop.

## Project structure

Files are grouped by their role, with each header next to its `.cpp` file.

```text
src/
├── main.cpp     # Starts the game and handles character selection
├── classes/     # Character classes, their base class, and IClasses
├── items/       # Equipment for each character class
├── shop/        # Shop, assortment, and IShop
├── player/      # Player creation
├── monsters/    # Monster data and combat
├── dungeon/     # Dungeon encounters
└── menu/        # Game menus and IMenu
```

## Build and run

Requires a C++11-compatible compiler, such as Clang or GCC.
From the project directory on macOS or Linux:

```sh
mkdir -p build
c++ -std=c++11 -pthread \
    -Isrc/classes -Isrc/items -Isrc/shop -Isrc/player \
    -Isrc/monsters -Isrc/dungeon -Isrc/menu \
    src/main.cpp src/*/*.cpp -o build/commandlinegame
./build/commandlinegame
```

Enter your name, choose a class using `1`–`4`, and follow the numbered menus.
Choose `4` in the main menu to exit.
