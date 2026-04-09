# Bashame's ROP Tools

A browser-based toolkit for Return-Oriented Programming (ROP) analysis and binary exploration, specially tailored for the Casio fx-580VN X architecture.

**Live Demo:** [https://tahoangphuc111.github.io/roptools/](https://tahoangphuc111.github.io/roptools/)

---

## 1. Find Gadget

Search for execution sequences (gadgets) within complete disassembly files.

* **Upload** an `.asm`, `.dis`, or `.txt` file containing assembly instructions.
* **Smart Search:** Use standard text or flexible wildcard `$` for registers (e.g., `l er$, [er$]`).
* **Results:** Gadgets automatically resolve endings (`pop pc`, `rt`, etc.), with simple controls to sort by length/address and copy blocks formatlessly.

## 2. Decompiler fx-580VN X

Reverse hexadecimal data back into its readable assembly instructions.

* **Decompile:** Input flat hex strings to identify routine addresses and memory sequences.
* **Automatic Analysis:** Recognizes known gadgets (200+ db entries), parsing nested `pop` arguments dynamically.
* **Views:** Toggle between Detailed flow mapping and Simple raw outputs for pasting into your exploit scripts.
