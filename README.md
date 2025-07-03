
# 🎲 8051 LCD + External Interrupt Dice Project

This project demonstrates how to use an **external interrupt (INT0)** on the **8051 microcontroller** to simulate the rolling of a dice and display the result on an **LCD screen**.

When the system starts, it shows the message **“Ready to roll?”** on the LCD. As soon as an external interrupt is triggered (like pressing a button), the program randomly selects a number between **1 and 6** and displays **“The number is: X”** where X is the dice value.

It’s a fun and simple way to explore interrupt handling, LCD interfacing, and delay generation using **pure 8051 Assembly language**.

---

## 🧩 Components Used

- 🧠 **8051 Microcontroller**  
- 💬 **16x2 LCD Display** (Alphanumeric)
- 🚨 **External Interrupt (INT0)** – usually triggered via push button
- ⏲ **Timer** – for generating delays
- ✨ Pull-up resistors, push button (for interrupt), power supply, etc.

---

## 💻 Code Functionality Breakdown

- `P1` (Port 1) is connected to the **LCD data pins**
- `P2.0` = **RS** (Register Select)  
- `P2.1` = **R/W** (Read/Write)  
- `P2.2` = **EN** (Enable)

The program does the following:
1. Initializes the LCD using standard command instructions.
2. Displays the message: **"Ready to roll?"**
3. Waits for an **INT0 interrupt** (external trigger)
4. On interrupt:
   - Picks a pseudo-random number (1 to 6)
   - Displays the string: **"The number is:"**
   - Then shows the selected number (`1` to `6`) on the LCD

---

## 📦 Project Files

- `interrupt_lcd.asm` – The complete assembly source code for this project.
- `README.md` – You're reading it!
- (Optional) `LICENSE` – MIT License to make the code open-source.

---

## ⚙️ Tools Used

- 🛠️ **Keil µVision IDE** for writing and simulating 8051 Assembly code  
- You can also view/edit the `.asm` file using any text editor (e.g., VS Code, Notepad++)

---

## 📌 Notes

- This project was originally tested using the Keil emulator.  
- If you no longer have Keil, you can still keep this code as a part of your GitHub portfolio or use online 8051 emulators.
- It's a great starting point for beginners learning microcontroller interrupts and LCD interfacing.

---

## 📜 License

This project is licensed under the **MIT License** — feel free to use, modify, and share it. Just don’t forget to give credit. 😊
