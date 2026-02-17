# Tic-Tac-Toe Game

A low-level implementation of the classic "Tic-Tac-Toe" game developed in Assembly language for the Von Neumann Simulator.

## Project Overview

The objective of this project is to implement a functional "Tic-Tac-Toe" game by managing Input/Output (I/O) devices through memory mapping. The program allows two players to interact with a 3x3 board through a simulated keyboard and screen.

## How to Play

The game follows a turn-based system for two players:

1. **Board Setup:** A 3x3 grid is drawn on the screen.
2. **Player 1 Turn:** The player is prompted to enter a Row and Column. If the position is valid and empty, an **"X"** is printed.
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

* **Language:** Assembly.
* **Architecture:** Von Neumann Simulator.
* **Virtual Peripherials:** Virtual Screen and Keyboard of the Von Neumann Simulator.

**Note:** Most of the Von Neumann Simulator interface is in **Spanish** as it was developed for a final project in the University of Oviedo (Spain).

## Dependencies

This project requires the **Von Neumann Simulator** environment and **Windows OS** to assemble and execute the source code.

## How to Run

Open the `VonNeumann.exe` application and the corresponding shell to the simuladorVN path. Do NOT use PowerShell to open the shell; instead use only CMD (type CMD in the Windows browser and go to the path with `cd C:\path\of\simuladorVN`).

### 1. Connect the Screen and Keyboard on the simulator
* **Reserve memory for peripherials:** Click on the **MEMORIA** button (bottom left), select the **Configurar** button and now remove the 32k module below by selecting the cross and clicking on it. Then click the **Aceptar** button.
* **Keyboard:** Navigate to `Utilidades -> Entrada/Salida -> Conectar Teclado`.
  * Nombre P.: _TECLAT_
  * Dir. Base: _B000_
  * Vector Int: _0_
  * Click the **Aceptar** button.
* **Screen:** Navigate to `Utilidades -> Entrada/Salida -> Conectar Pantalla`.
  * Nombre P.: _PANTALLA_
  * Dir. Base: _A000_
  * Click the **Aceptar** button.
* If you want to disconnect a peripherial you need to navigate to `Utilidades -> Entrada/Salida -> Desconectar Periférico`, select the corresponent peripherial and click the **Desconectar** button.

### 2. Compile
  ```bash 
  Ensambla.exe src\ec2_pra_2.ens
  ```

### 3. Run
* Navigate to `Archivo -> Abrir` and select the generated `ec2_pra2.eje` file in the ~simuladorVN\src path.
* Then navigate to `Ejecución -> Run`.
* To stop the program navigare to `Ejecución -> Parar`.

## Technical Note (Language)
The source code, variables names, internal comments and output console prints are written in **Catalan**, as it was an academic project for the University of Lleida (UdL) as part of the **Computer Science degree (Estructura de Computadors II, 2024-2025)**. This documentation is provided in English so more people can understand the project.

## Credits
The Von Neumann SImulator was developed in the University of Oviedo by Diego Alonso López under the direction of Manuel Campos López.

---
**Developed by:** Eric Buenavida Crespo.
