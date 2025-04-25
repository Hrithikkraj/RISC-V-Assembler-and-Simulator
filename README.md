# 🛠️ Assembler and Simulator Testing Framework – 2024

This project provides a testing framework for validating **Assembler** and **Simulator** implementations for a custom ISA. It supports both **simple** and **hard** test cases, enabling students to validate correctness independently for each component.

---

## 📁 Project Structure

```
tests/
├── assembly/
│   ├── simpleBin/        # Input assembly files (simple tests)
│   ├── hardBin/          # Input assembly files (hard tests)
│   ├── errorGen/         # Error-generating assembly cases (for negative testing)
│   ├── bin_s/            # Reference machine code for simpleBin
│   ├── bin_h/            # Reference machine code for hardBin
│   ├── user_bin_s/       # Student-generated machine code from simpleBin
│   └── user_bin_h/       # Student-generated machine code from hardBin
├── bin/                  # Student-generated simulator traces
└── traces/               # Correct simulator trace outputs
```

---

## 🧪 Testing Overview

### 🔧 Assembler Tests

- **10 Simple Tests**  
  ✅ Weight: `0.1` × 10

- **5 Hard Tests**  
  ✅ Weight: `0.2` × 5

### 🔩 Simulator Tests

- **5 Simple Tests**  
  ✅ Weight: `0.4` × 5

- **5 Hard Tests**  
  ✅ Weight: `0.8` × 5

> 💡 Assembler and simulator tests are **independent** and can be tested separately.

---

## 🚀 Usage Instructions

### ⚙️ Assembler

**Input:** Assembly code file (`.txt`)  
**Output:** Machine code file (`.txt`)

**Format:**
```bash
$ python3 Assembler.py input_file.txt output_file.txt
```

### ⚙️ Simulator

**Input:** Machine code file (`.txt`)  
**Output:** Simulator trace file (`.txt`)

**Format:**
```bash
$ python3 Simulator.py input_file.txt output_file.txt
```

---

## 🗂️ Setup Instructions

### 🧾 Assembler

1. **Rename your assembler file** to:  
   ```
   Assembler.py
   ```

2. **Place it inside:**  
   ```
   SimpleAssembler/
   ```

3. **Run using:**

   - **Linux:**
     ```bash
     $ python3 src/main.py --no-sim --linux
     ```

   - **Windows:**
     ```cmd
     > python3 src\main.py --no-sim --windows
     ```

---

### 🧾 Simulator

1. **Rename your simulator file** to:  
   ```
   Simulator.py
   ```

2. **Place it inside:**  
   ```
   SimpleSimulator/
   ```

3. **Run using:**

   - **Linux:**
     ```bash
     $ python3 src/main.py --no-asm --linux
     ```

   - **Windows:**
     ```cmd
     > python3 src\main.py --no-asm --windows
     ```

---

## ✅ Notes

- All input/output files **must** use `.txt` extension.
- Ensure the directory structure remains intact for correct test evaluation.
- This framework supports only **Python** implementations.

