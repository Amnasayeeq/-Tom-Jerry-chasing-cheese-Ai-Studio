
# 🐭 Tom & Jerry: The Great Cheese Chase

### Reinforcement Learning — Q-Learning vs Deep Q-Network (DQN)
**AI Studio Final Project · B144**

Jerry (RL agent) navigates a 16×18 grid house, collects 10 cheese pieces, and evades Tom the cat (BFS pathfinder). Two algorithms compete: classic Q-Learning vs neural-network DQN. A fully playable browser game with 7 progressive difficulty levels is also included.

---

## 🎮 Play the Game

The game runs directly in the browser — no install needed.
* **Host on GitHub Pages:** Push `index.html` to a repo → enable Pages → free URL forever.
> 🎮**Controls:** Arrow keys or on-screen buttons  
> 🥅**Goal:** Collect all cheese before Tom catches you!

---

## Project Summary

| Item | Detail |
| :--- | :--- |
| **Course** | B144: AI Studio |
| **Subject Code** |B144|
| **Algorithms** | Q-Learning (dict Q-table) + DQN (PyTorch) |
| **Environment** | Custom 16×18 grid — Tom & Jerry house |
| **State space** | 294,912 states (position × 10-bit cheese mask) |
| **Training** | 3,000 episodes per algorithm |
| **Game levels** | 7 levels, Tom speeds up each level |

---

## The House

```
 J = 🐭Jerry start (1,1)
 T = 😾 Tom start (14,16)
 C = Cheese (×10)
  █ = Wall

  |██████████████████|
  |█JC·█···C·█··C···█|
  |█·█·█·██·██·█·██·█|
  |█·█··C·█····█····█|
  |█·████·███·███·█·█|
  |█········C·····█·█|
  |███·███·███·██·█·█|
  |█···█C····█··█···█|
  |█·█···██··C·██·█·█|
  |█·███·█··██·█··█·█|
  |█···C·······C····█|
  |█·██·██·██·██·██·█|
  |█··█··█··█·······█|
  |█·██·███·███·███·█|
  |█········C······T█|
  |██████████████████|
```
---
## Algorithms
1. Q-Learning
   -1. Q-Learning
   -Bellman update:
     *Q(s,a) \leftarrow Q(s,a) + \alpha [r + \gamma \cdot \max_{a'} Q(s',a') - Q(s,a)*
   -Epsilon
   -Evasion
   
2. Deep Q-Network (DQN)
   - Network
   -State encoding
   -Experience Replay
   -Target Network 
   -Adam optimizer

3. Tom's Training
   -Tom's AIBFS pathfinding
   -Speed control
---

Level Progression

| Level | Tom | Delay | Cheese target |
|--------|---------|---------|---------|
| 1 | sleepy tom |J(8 steps)->T(1 steps)| 5 |
| 2 | yawming tom | J(6 steps)->T(1 steps) | 6 |
| 3 | strectching tom | J(5 steps)->T(1 steps) |7 |
| 4 | strotting tom | J(4 steps)->T(1 steps) | 8 |
| 5 | jogging tom | J(3 steps)->T(1 steps) | 9 |
| 6 | running tom | J(2 steps)->T(1 steps) | 10 |
| 7 | sprinting tom | J(1 steps)->T(1 steps) | 10 |


