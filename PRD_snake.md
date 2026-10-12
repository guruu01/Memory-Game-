# PRD: Snake Game

## 1. Overview
This product requirement document defines the creation of a Snake game as a lightweight browser-based single-file web app. The game will be built with HTML, CSS, and JavaScript and designed to run directly in a browser without any external dependencies.

The purpose of the game is to provide a simple, nostalgic arcade experience where a player controls a snake, eats food, grows longer, and avoids colliding with walls or itself.

## 2. Product Goal
Create a playable Snake game that feels polished, responsive, and easy to understand while remaining lightweight and self-contained.

The game should support:
- keyboard controls
- score tracking
- increasing difficulty over time
- restart flow
- local best score persistence
- browser-based play without setup dependencies

## 3. User Need
Users want a quick, fun, arcade-style game that feels familiar and easy to play. They expect immediate interaction, simple controls, instantly understandable rules, and a satisfying progression as the snake grows.

## 4. Scope
### In Scope
- Single-page Snake game
- Board rendering using HTML/CSS/JS
- Keyboard controls with arrow keys and WASD
- Food spawning and collision detection
- Score and best score tracking
- Restart and replay flow
- Game over state with clear message
- Responsive layout for desktop and small screens

### Out of Scope
- Multiplayer mode
- Sound effects
- Advanced animations or physics engines
- External libraries or frameworks
- Server-side persistence or account login

## 5. User Stories
1. As a player, I want to move the snake using the keyboard so I can play quickly.
2. As a player, I want to eat food so the snake grows and my score increases.
3. As a player, I want the game to end when I hit a wall or my own body so the rules are clear.
4. As a player, I want a restart button so I can play again immediately.
5. As a player, I want my best score saved so I can try to beat it later.

## 6. Functional Requirements
### 6.1 Game Board
- The game shall render on a square board with a fixed grid size.
- Each snake segment and food item shall occupy a single grid cell.
- The board shall update continuously during gameplay.

### 6.2 Snake Movement
- The snake shall start with a defined initial length and position.
- Movement shall be controlled by arrow keys or WASD.
- The snake shall not reverse direction immediately into its own body.
- Movement speed shall remain consistent and predictable during regular play.

### 6.3 Food and Growth
- Food shall spawn in a random empty cell.
- When the snake consumes food, it shall grow by one segment.
- The score shall increase each time food is eaten.

### 6.4 Game Over
- The game shall end when the snake hits the wall or collides with itself.
- A game-over message shall be shown to the user.
- The board shall stop moving after game over.

### 6.5 Restart and Replay
- There must be a restart button or keyboard action to begin a new round.
- A new game shall reset the score, snake position, and food placement.

### 6.6 Score Tracking
- The current score shall be displayed during gameplay.
- The best score shall be saved in localStorage and updated automatically.

## 7. Non-Functional Requirements
### 7.1 Performance
- The game should run smoothly in modern desktop browsers.
- The game loop should not produce noticeable lag on typical hardware.

### 7.2 Accessibility
- The interface should maintain visible contrast and readable controls.
- Keyboard support should be present for primary interaction.

### 7.3 Maintainability
- The game should be simple, readable, and contained in one HTML file for easy editing.
- CSS should use a consistent visual palette and class structure.

## 8. UX and Visual Requirements
- The game should have a clean arcade-style aesthetic.
- The snake and food should be visually distinct and easy to understand.
- The board should center nicely on the page with clear score information.
- The game-over state should be obvious without being overly complicated.

## 9. Acceptance Criteria
The feature is complete when all the following are true:

1. The user can start a new Snake game from the browser.
2. The snake can be moved using keyboard controls.
3. Food appears at random and is collectable.
4. Eating food increases score and length.
5. Colliding with walls or the snake body ends the game.
6. A button or action allows replay.
7. Best score persists across page reloads.
8. The game works without external dependencies.

## 10. QA Test Plan
### Functional Testing
- Start the game and verify movement begins correctly
- Move left, right, up, and down without invalid reversal
- Eat food and confirm score increments
- Continue until collision and confirm game-over state
- Restart and verify complete reset

### Edge Cases
- Try moving directly backward into self
- Move quickly between key presses to ensure reliability
- Reload page and confirm best score remains

### Visual Testing
- Ensure board renders properly on desktop and smaller screens
- Verify text and colors remain readable
- Check that the score panels and controls align correctly

## 11. Risks and Constraints
- Input timing must be handled carefully to prevent reverse-direction bugs.
- The game should avoid overly complex logic in a single-file implementation.
- The board size needs to remain manageable for both gameplay and readability.

## 12. Recommendation
This is a strong fit for a single-file browser game because the game mechanics are straightforward, the gameplay is familiar, and the implementation remains easy to maintain in one document.

## 13. Success Metric
The project is successful if the game is immediately playable, responsive, and enjoyable without setup friction, and if the player can clearly complete a full game loop from start to finish.
