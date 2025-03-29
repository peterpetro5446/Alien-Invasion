# Alien Encounter – Interactive Simulation

This is a short C program that simulates an interactive alien encounter, inspired by a peer’s scenario in a programming assignment. The outcome of your intergalactic meeting depends on your choices, your tools, and a bit of luck.

---

## Scenario

> You find yourself in the middle of an unexpected alien encounter.  
> The success of your interaction with extraterrestrial beings depends on specific conditions:
- If you use a **universal translator** and it works **successfully**, and
- You offer a **unique Earth souvenir**,  
→ The encounter is **friendly**.

Otherwise:
- If the translator **malfunctions**, or
- You **fail to offer a souvenir**, or
- You attempt to **run away or attack**,  
→ The encounter becomes **hostile**.

---

##  Program Behavior

The program presents a menu of options when run:
1. Attempt to communicate without translator  
2. Use a universal translator  
3. Run away  
4. Attack the aliens  

Depending on your input and randomized translator reliability, you'll get different outcomes. The program ends either in peace… or not.

---

##  Features

- Input validation with retry limit
- Randomized translator malfunction simulation
- Friendly or hostile endings based on decision path
- Creative alien-language flavor text for immersion

---

## 🔧 Compile & Run

### Compile with `gcc`:
```bash
gcc -o alien_encounter alien_encounter.c
