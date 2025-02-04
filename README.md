# 🐍 Pygame Snake Game  

A **classic Snake game** built using the **Pygame module**, featuring **five levels** with increasing difficulty and special **bonus fruits**. The game graphics are handled by importing images and placing them on respective rectangles using Pygame.  

---
## 🎥 Screenshots & Gameplay  
![Gameplay Demo](https://github.com/GulmurodY/pygame-snake-game/blob/patch1/pygame.gif)
---

## 🚀 Installation  

To install the **Pygame** module, follow these steps:  

1. Download and install **Python 3** from the [official website](https://www.python.org/) if you haven’t already.  
2. Install Pygame using pip:  
```
pip3 install pygame
```

---

## 🎮 Running the Game  

1. Clone the repository and navigate to the project folder:  
```
git clone https://github.com/yourusername/snake-game.git
cd snake-game
```


2. Run the game using:  

```
python3 main.py
```


---

## 🐍 Snake Class  

The **`Snake`** class defines the behavior of the snake in the game.  

### 🛠 Methods:  

- **`__init__()`** – Initializes the snake with a color.  
- **`draw_snake()`** – Draws the snake on the screen.  
- **`update_head_graphics()`** – Updates the appearance of the snake’s head.  
- **`update_tail_graphics()`** – Updates the appearance of the snake’s tail.  
- **`move_snake()`** – Moves the snake in the current direction. If it eats a fruit, its body grows.  
- **`add_block()`** – Adds a new block to the snake's body when required.  
- **`play_crunch_sound()`** – Plays a sound effect when the snake eats a fruit.  

---

## 🍏 Fruit Class  

The **`Fruit`** class manages different types of bonus fruits.  

### 🍊 Available Fruits:  

- **Apple 🍏** – Worth **1 point**  
- **Orange 🍊** – Worth **5 points**  
- **Watermelon 🍉** – Indicates **victory**  

### 🛠 Methods:  

- **`__init__()`** – Initializes a new fruit.  
- **`draw_apple()`** – Draws an apple.  
- **`draw_orange()`** – Draws an orange.  
- **`draw_watermelon()`** – Draws a watermelon.  
- **`randomize()`** – Places the fruit at a random position on the grid.  

---

## 🌿 Grass Class (Level Maps)  

The **`Grass`** class manages the different **level designs** and **border walls**.  

### 🛠 Methods:  

- **`__init__()`** – Stores the border coordinates for different levels.  
- **`draw_grass()`** – Draws the level map on the screen.  

---

## 🕹 Main Game Logic  

The **`Main`** class defines the game logic and behavior in each game loop iteration.  

### 🛠 Key Methods:  

- **`__init__()`** – Initializes game elements (Snake, Fruit, Grass).  
- **`update()`** – Updates game elements like snake movement and collision detection.  
- **`draw_elements()`** – Draws all game components (snake, fruit, grass).  
- **`check_collision()`** – Detects when the snake eats a fruit, randomizes fruit placement, and increases speed.  
- **`check_next_level()`** – Determines if the player advances to the next level.  
- **`pass_to_lvlX()`** – Resets the snake and speed when transitioning between levels.  
- **`check_fail()`** – Detects game-over conditions.  
- **`update_record()`** – Updates the high score table.  
- **`game_over_output()`** – Displays the **Game Over** screen, plays sounds, and resets game state.  
- **`draw_top_score()`** – Displays leaderboard scores.  
- **`draw_score()`** – Shows the player's current score in the bottom-right corner.  
- **`game_won()`** – Displays **"YOU WON"** message when all levels are completed.  
- **`pause()`** – Pauses the game. Players can press **C** to continue or **Q** to quit.  
- **`check_game_won()`** – Determines if the player has completed all levels.  

---

## 🎯 Game Mechanics & Features  

- **Grid-Based Movement** – The game uses a **cell grid system**, where the snake consists of square blocks.  
- **Customizable Speed** – The snake’s speed starts at **6** and increases upon fruit consumption.  
- **Frame Rate Control** – A **Pygame clock** keeps track of FPS to ensure smooth gameplay.  
- **Sound Effects** – Pygame’s **mixer module** is used to play **crunch** sounds when the snake eats a fruit.  
- **Key Press Management** – Prevents multiple key inputs from being registered simultaneously.  

---

## 🔄 Game Loop  

The game loop is responsible for handling:  

- **User input** via `pygame.event`  
- **Updating the snake's direction**  
- **Checking collisions**  
- **Drawing game elements**  
- **Handling level progression and game-over scenarios**  

