# ConnectN: A Command-Line Game in C

ConnectN is a fully functional, command-line N-in-a-row game written entirely in C. This project was developed as a core assignment for the ECS 036A curriculum at UC Davis and serves as a demonstration of fundamental C programming principles, including dynamic memory management, pointer manipulation, and algorithmic logic.

The game allows two players to compete on a customizable `N x M` board, aiming to get `K` pieces in a row to win.

---

## Key Features

*   **Dynamic Game Board:** The game board is created at runtime using `malloc`, allowing for customizable board dimensions (`rows`, `columns`) and win conditions (`number to connect`) specified by the user through command-line arguments.
*   **Robust Input Validation:** Implements comprehensive error handling to gracefully manage invalid user inputs, incorrect command-line arguments, and invalid move attempts (e.g., placing a piece in a full column).
*   **Complex Win-Condition Logic:** Features an efficient algorithm to check for a win condition after every move. It systematically checks for horizontal, vertical, and both diagonal victories across the entire `N x M` grid.
*   **Manual Memory Management:** All dynamically allocated memory for the game board and other data structures is meticulously tracked and explicitly freed using `free()` at the end of the program to prevent memory leaks.

---

## How to Compile & Run

This project uses a `Makefile` for easy compilation.

1.  **Clone the repository:**
    ```bash
    git clone [URL of your ConnectN repo]
    cd [ConnectN repo name]
    ```

2.  **Compile the program:**
    ```bash
    make
    ```

3.  **Run the game:**
    The program is run with three command-line arguments: `num_rows`, `num_cols`, and `num_pieces_to_win`.
    ```bash
    ./connectn 6 7 4  // This will start a standard 6x7 Connect Four game.
    ```

---

## Key Learnings & Takeaways

This project was a profound, hands-on lesson in the challenges and power of low-level programming in C. The most significant challenge was debugging a critical memory leak that caused a segmentation fault during the win-check sequence. After two days of intensive debugging using **GDB**, I successfully isolated and fixed the bug, which was a true "aha!" moment in my understanding of pointers and memory.

This experience solidified my passion for systems programming and taught me the discipline required to build robust, reliable software from the ground up.
