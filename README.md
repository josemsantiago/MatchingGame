# MatchingGame
### Spot the Difference Browser Game

An interactive web-based "spot the difference" game that demonstrates advanced DOM manipulation, event handling, and JavaScript programming concepts.

## Overview

This browser game challenges players to find the extra smiling face that appears only on the left side. The game dynamically generates faces, creates visual differences between two panels, and progressively increases difficulty with each successful round.

## Game Mechanics

### 🎯 Objective
Find and click the extra smiling face that appears only on the left panel. The right panel is missing one face, creating the "difference" to spot.

### 🎮 Gameplay Flow
1. **Setup**: Two side-by-side panels display randomly positioned smiley faces
2. **Generation**: Left panel shows N faces, right panel shows N-1 faces
3. **Challenge**: Player must identify and click the extra face on the left
4. **Progression**: Successful clicks advance to next level with 5 additional faces
5. **Game Over**: Clicking wrong areas results in game over and restart

### 📊 Difficulty Progression
- **Level 1**: 5 faces
- **Level 2**: 10 faces
- **Level 3**: 15 faces
- **Continues**: +5 faces per level

## Technical Implementation

### JavaScript Features
- **Dynamic DOM Generation**: Creates image elements programmatically
- **Random Positioning**: Places faces randomly within 400x400 pixel area
- **Event Handling**: Click listeners for game interaction
- **Progressive Difficulty**: Automatic level advancement
- **Game State Management**: Tracks current level and face count

### DOM Manipulation
```javascript
// Core functions:
generateFaces(numberOfFaces)    // Creates and positions face images
nextLevel()                     // Advances difficulty and resets panels
gameOver()                      // Handles game termination and reset
```

### CSS Styling
- **Panel Layout**: Two 500x500 pixel game areas
- **Absolute Positioning**: Precise face placement
- **Visual Separation**: Border between left and right panels
- **Responsive Design**: Fixed dimensions for consistent gameplay

## How to Play

1. **Start**: Open `matching-game.html` in a web browser
2. **Observe**: Study both panels to spot differences
3. **Click**: Click on the extra face that appears only on the left
4. **Progress**: Successfully find faces to advance levels
5. **Challenge**: Game gets harder with more faces each level

## File Structure

```
MatchingGame/
├── matching-game.html     # Complete game implementation
└── README.md             # This documentation
```

## Browser Requirements

- **JavaScript**: Must be enabled for game functionality
- **Modern Browser**: Chrome, Firefox, Safari, Edge recommended
- **Image Support**: Browser must support PNG image format
- **DOM Support**: Full DOM manipulation capabilities required

## Known Limitations

⚠️ **Missing Asset**: The game references `images/smile.png` but this file is not included in the repository. You'll need to:
1. Create an `images/` directory
2. Add a `smile.png` file (smiley face image)
3. Ensure the image is appropriately sized for the game

## Educational Value

This project demonstrates:
- **DOM Manipulation**: createElement, appendChild, removeChild methods
- **Event Handling**: Click event listeners and callback functions
- **Random Number Generation**: Math.random() for positioning
- **Game Logic**: State management and progression systems
- **CSS Positioning**: Absolute positioning and layout techniques

## Sample Code Structure

```javascript
// Game variables
let numberOfFaces = 5;
const leftPanel = document.getElementById('leftSide');
const rightPanel = document.getElementById('rightSide');

// Core game functions
function generateFaces() {
    // Generate random face positions
    // Create image elements
    // Clone to right panel (excluding one)
}

function nextLevel() {
    // Increase difficulty
    // Reset panels
    // Generate new faces
}
```

## Customization Options

### Visual Modifications
- Change face images by replacing `smile.png`
- Modify panel sizes by adjusting CSS dimensions
- Update color scheme in CSS styling
- Add sound effects for interactions

### Gameplay Modifications
- Adjust starting face count (change initial `numberOfFaces`)
- Modify difficulty progression (change increment value)
- Add timer for time-based challenges
- Implement scoring system

## Debugging Notes

If faces don't appear:
1. Check that `images/smile.png` exists
2. Verify image path is correct
3. Ensure browser console shows no errors
4. Check that JavaScript is enabled

## Future Enhancements

Potential improvements:
- **Multiple Image Types**: Different shapes, colors, sizes
- **Timed Challenges**: Add countdown timers
- **Scoring System**: Points based on speed and accuracy
- **Sound Effects**: Audio feedback for interactions
- **Mobile Support**: Touch-friendly responsive design
- **Difficulty Settings**: Easy, medium, hard modes

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

*Note: This game requires a `smile.png` image file in an `images/` directory to function properly.*
