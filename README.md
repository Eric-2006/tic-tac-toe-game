# Tic-Tac-Toe Game

A low-level implementation of the classic "Tic-Tac-Toe" game developed in Assembly language for the Von Neumann Simulator.

## Project Overview

The objective of this project is to implement a functional "Tic-Tac-Toe" game by managing Input/Output (I/O) devices through memory mapping. The program allows two players to interact with a 3x3 board through a simulated keyboard and screen.

## How to Play

The game follows a turn-based system for two players:

1. **Board Setup:** A 3x3 grid is drawn on the screen.
2. **Player 1 Turn:** The player is prompted to enter a Column and Row. If the position is valid and empty, an **"X"** is printed.
3. **Player 2 Turn:** Similar to Player 1, the player enters coordinates. If valid, an **"O"** is printed.
4. **Validation:** The program automatically rejects invalid coordinates or positions that are already occupied, asking for new input.

## Determining the Winner

The game uses a specific numerical logic to determine the winner based on the three board vectors (`fila1`, `fila2`, `fila3`):

* **Player 1 Strategy:** Every move stores the value **1** in the chosen position.
* **Player 2 Strategy:** Every move stores the value **5** in the chosen position.
* **Win Condition:** The program checks rows, columns, and diagonals. 
    * A total sum of **3** in any line indicates Player 1 has won.
    * A total sum of **15** in any line indicates Player 2 has won.
* **Draw:** If the board is full and no player has reached the required sum, the game ends in a tie.

## Technologies Used

* **Language:** Assembly (ASM).
* **Architecture:** Von Neumann Simulator.
* **Virtual Peripherials:** Virtual Screen and Keyboard of the Von Neumann Simulator.

## Dependencies

This project requires the **Von Neumann Simulator** environment and **Windows OS** to assemble and execute the source code.

## How to Run

### 1. Compile (from simuladorVN file)
  ```bash 
  type > Ensambla src/ec2_pra2.ens
  ```
### 2 Connect the Screen and Keyboard
* **Keyboard** Utilidades -> Entrada/Salida -> Conectar Teclado
  * Nombre P.: TECLAT
  * Dir. Base 0B000h
* **Screen** Utilidades -> Entrada/Salida -> Conectar Pantalla
  * Nombre P.: PANTALLA
  * Dir. Base 0A000h
### 3. Run
* Archivo -> Abrir -> Now select the `ec2_pra2.eje` file

### Technical Specifications
* **Program Origin:** `100h`.
* **Memory Map:** Keyboard at `0B000h` and Screen at `0A000h`.

## Technical Note (Language)
The source code, variables, internal comments and output console prints are written in **Catalan**, as it was an academic project for the University of Lleida (UdL) as part of the **Computer Science degree (Estructura de Computadors II, 2024-2025)**. This documentation is provided in English for universal portfolio visibility.

## Credits
The Von Neumann SImulator was developed in the University of Oviedo by Diego Alonso López under the direction of Manuel Campos López.

---
**Developed by:** Eric Buenavida Crespo.
