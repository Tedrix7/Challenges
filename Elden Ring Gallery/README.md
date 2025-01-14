# Interactive Grid UI with Custom Cursor (ELDEN RING)

This project implements an interactive grid-based UI with a custom mouse cursor and smooth animations. 
It uses JavaScript, CSS, and libraries like Anime.js and imagesLoaded to create a visually appealing and responsive experience. 
I used ChatGPT to help me with JavaScript.(That's why I left the green lines)

## Features

### Custom Mouse Cursor
- Replaces the default cursor with a custom design.
- Includes dynamic elements (`.cursor__inner--circle`, `.cursor__inner--text`) that:
  - Scale and fade based on user interactions.
  - Toggle between different states (circle and cross).

### Dynamic Grid Layout
- A grid of items with interactive animations that respond to mouse movements.
- Hovering over an item displays its title near the cursor.
- Clicking on an item reveals detailed content and hides the grid.

### Smooth Animations
- Utilizes Anime.js for fade, scale, and staggered animations.
- Grid translates dynamically based on the mouse position along the y-axis.

### Responsive Design
- Grid and cursor adapt to window resizing.
- Dimensions and scaling are recalculated dynamically for seamless transitions.

### Lazy Loading and Image Preloading
- Preloads images using the `imagesLoaded` library to ensure smooth rendering and transitions.

## Libraries Used
- **Anime.js**: For managing animations.
- **imagesLoaded**: To preload images and handle background image loading.
- **CSS Grid**: For flexible and responsive layout structure.

## How It Works

### Math Utilities
```javascript
const MathUtils = {
    lineEq: (y2, y1, x2, x1, currentVal) => {
        var m = (y2 - y1) / (x2 - x1), b = y1 - m * x1;
        return m * currentVal + b;
    },
    lerp: (a, b, n) => (1 - n) * a + n * b
};
```
These functions handle linear interpolation and value mapping.

### Cursor Effects
The `CursorFx` class manages the custom cursor's position, scale, and opacity. It follows mouse movements and interacts with grid items dynamically.

### Grid
The `Grid` class handles layout, animations, and interactions:
- Clicking on an item triggers animations that fade out the grid and reveal detailed content.
- Returning to the grid view reverses the animations.

### Image Preloading
Images are preloaded to ensure smooth transitions without incomplete rendering.

## Usage

### Setup
1. Clone the repository:
2. Navigate to the project directory:
3. Open `index.html` in your browser.

### File Structure
- **HTML**: The main structure of the grid and content.
- **CSS**: Styles for the grid, custom cursor, and animations.
- **JavaScript**:
  - `CursorFx`: Manages the custom cursor.
  - `Grid`: Handles the grid layout and animations.
  - `MathUtils`: Provides helper functions for interpolation.

### Customization
- Modify grid items in the HTML to add new images or titles.
- Update CSS variables for layout adjustments (e.g., number of rows and columns).
- Extend `CursorFx` and `Grid` classes for additional animations or interactions.

## Enhancements

### Error Handling
- Handle scenarios where images fail to load gracefully.
- Add checks for animation exceptions.

## Dependencies
- **Anime.js**: [Anime.js documentation](https://animejs.com/)
- **imagesLoaded**: [imagesLoaded documentation](https://imagesloaded.desandro.com/)

