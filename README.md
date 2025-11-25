# **Pixel Project**
*A color-expansion and territory-domination simulation built in Processing.*

---

## **Overview**
The **Pixel Project** simulates four competing colors—**Red**, **Blue**, **Green**, and **Yellow**—spreading and fighting across a **10×10 grid**. Each color starts in a corner, expands outward following directional rules, and eventually enters a combat phase until one color dominates all **100 tiles**.

---

## **Features**
- **10×10 grid** of dynamically colored cubes  
- **Expansion phase** where colors fill empty (white) tiles  
- **Combat phase** where colors overwrite each other  
- **Win detection** when any color reaches **100 tiles**  
- **Visual progression** with a short delay between turns

---

## **How It Works**

### **Grid Initialization**
Each color begins at a corner:  
- **Red** → top-left (0,0)  
- **Blue** → top-right (0,9)  
- **Green** → bottom-left (9,0)  
- **Yellow** → bottom-right (9,9)

All other cells begin as **white / unclaimed**.

### **Expansion Phase**
During the first **9 cycles**, each color expands only into **uncolored** tiles based on movement rules:

- **Red** → right & down  
- **Blue** → left & down  
- **Green** → right & up  
- **Yellow** → left & up

### **Combat Phase**
After the grid fills:

- A random “fight type” determines which colors attempt attacks  
- Colors can overwrite **already-colored** tiles  
- When a color reaches **99 tiles**, special logic attempts a final conversion  
- When a color reaches **100**, the simulation ends

A centered message displays the winner, for example:  
**"Red won!"**

---

## **File Structure**
The project is contained in a single Processing `.pde` sketch and organized as:

- **Main sketch**
  - `setup()`  
  - `draw()`  
- **Cube class** — stores color/state and draws each square  
- **Grid class** — handles initialization, expansion, combat, counting, and rendering

---

## **How to Run**
1. Install **Processing** from: https://processing.org/  
2. Create a new sketch in the Processing IDE  
3. Paste the full code into the sketch (`.pde`) file  
4. Click **Run** ▶

---
<img width="309" height="309" alt="Screenshot 2025-11-25 at 4 19 18 PM" src="https://github.com/user-attachments/assets/d3d1e5ff-235f-4061-9cff-f5ce624ccd64" />
<img width="309" height="309" alt="Screenshot 2025-11-25 at 4 19 29 PM" src="https://github.com/user-attachments/assets/82362b27-afff-4daf-9a76-e2683ef1babe" />
<img width="309" height="309" alt="Screenshot 2025-11-25 at 4 19 47 PM" src="https://github.com/user-attachments/assets/0957c554-884b-45fa-abbf-e4ea440f6a5c" />

