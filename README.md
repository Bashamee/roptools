# ⚡ Bashame's ROP Tools
Runs entirely in your browser – access at:  
🔗 [https://bashamee.github.io/roptools/](https://bashamee.github.io/roptools/)

---

## 🧰 Tools

### 1. 🔍 Find Gadget – Search ROP gadgets in disassembly files

- **Upload** a disassembly file (`.txt`, `.asm`, `.dis`) – each line contains an instruction and address.
- **Search by instruction sequence**:
  - One instruction per line (e.g. `pop er`, `pop pc`).
  - Supports **wildcard `$`** for register numbers:  
    `l er$, [er$]` matches `l er10, [er8]`, `l er0, [er2]`, …
  - Without `$`, matching is **prefix‑based**: `pop er` matches `pop er0`, `pop er12`, …
- **Results**: lists gadgets ending with `pop pc`, `rt` or `rti`.  
  Each gadget shows address, line range, and length.
- **Sort**: by address or by length.
- **Copy**: individual gadget or all.

### 2. 📟 Decompiler fx‑580VN X – Convert hex to assembly

- **Enter** hex code (with or without spaces) of an ROP program.
- **Automatic analysis**:
  - Detects `call` instructions (hex pattern `ZZ YY X? 30`) and maps them to known gadget names (database of 200+ gadgets).
  - Extracts data (word/byte) following each `call` based on the number of `pop` operations inside the gadget.
- **Two display modes**:
  - **Detailed**: shows each item (hex → arrow → name/value → RAM address), with a 🔄 button to toggle raw hex.
  - **Simple**: prints only gadget names or hex values.
- **Custom start address** (default `0xD730`).
- **Copy** the result to clipboard.

---
