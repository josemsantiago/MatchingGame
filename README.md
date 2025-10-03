# MatchingGame
### Spot the Difference Browser Game

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-blue)
![Status](https://img.shields.io/badge/status-active-success)

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

1. **Start**: Open `index.html` in a web browser
2. **Observe**: Study both panels to spot differences
3. **Click**: Click on the extra face that appears only on the left
4. **Progress**: Successfully find faces to advance levels
5. **Challenge**: Game gets harder with more faces each level

## File Structure

```
MatchingGame/
├── index.html            # Complete game implementation
├── images/
│   └── smile.svg         # Smiley face image
└── README.md             # This documentation
```

## Browser Requirements

- **JavaScript**: Must be enabled for game functionality
- **Modern Browser**: Chrome, Firefox, Safari, Edge recommended
- **Image Support**: Browser must support SVG image format
- **DOM Support**: Full DOM manipulation capabilities required

## Assets

✅ The game includes `images/smile.svg` - a smiley face image used for the game pieces.

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
1. Check that `images/smile.svg` exists
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

## Screenshots

> **Note:** Screenshots will be added soon. To play the game immediately, open `index.html` in any web browser - no installation required!

## Troubleshooting

### Common Issues

**Issue:** Smiley faces don't appear on the page

**Solution:** Verify that `images/smile.svg` exists in the correct directory. Check browser console (F12) for 404 errors. Ensure the file path in the JavaScript matches your directory structure.

---

**Issue:** Game doesn't reset after clicking wrong area

**Solution:** The game restarts automatically when you click outside a valid face. If this doesn't work, refresh the page manually. Check browser console for JavaScript errors.

---

**Issue:** Faces overlap and are hard to click

**Solution:** This occurs more frequently at higher levels with many faces. Try clicking precisely on the center of each face. As difficulty increases, overlapping is expected behavior.

---

**Issue:** Game becomes too difficult at higher levels

**Solution:** The difficulty increases by 5 faces per level. To adjust difficulty, modify the `numberOfFaces` increment in the `nextLevel()` function. For easier gameplay, change it to increment by 3 or 4 instead of 5.

---

**Issue:** JavaScript errors in console

**Solution:** Ensure you're using a modern browser (Chrome 80+, Firefox 75+, Safari 13+). Check that JavaScript is enabled. Clear browser cache and reload the page.

For additional help, check the browser console for specific error messages or verify the file structure matches the expected layout.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add YourFeature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

**Suggested improvements:**
- Add timer for speed-based challenges
- Implement scoring system with leaderboards
- Add sound effects for correct/incorrect clicks
- Create difficulty settings (easy, medium, hard)
- Add different image themes (animals, shapes, emojis)
- Implement mobile touch optimization
- Add visual effects and animations

## Contact & Support

- **Author**: José Santiago Echevarria
- **Issues**: Report bugs or suggest features via [GitHub Issues](https://github.com/josemsantiago/MatchingGame/issues)
- **Project Type**: Educational browser game demonstrating DOM manipulation, event handling, and game state management
- **Tech Focus**: Vanilla JavaScript, dynamic HTML generation, absolute CSS positioning, and recursive game logic

---

*Note: This game uses `smile.svg` from the `images/` directory for the game pieces.*
