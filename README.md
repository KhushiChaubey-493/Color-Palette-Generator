# Color Palette Generator

A simple and interactive **Color Palette Generator** built using **HTML, CSS, and JavaScript**. The application generates a palette of four random HEX colors and displays them as visually distinct color blocks. Users can generate a new palette and copy individual HEX color values directly to the clipboard.

## Features

* Generates a palette containing **four random colors**.
* Generates valid **6-digit HEX color codes**.
* Displays each generated color as a visual color block.
* Shows the HEX value of each generated color.
* Copy individual HEX color values with a click.
* Displays a confirmation message after copying a color.
* Generate a new palette with the **Generate Colors** button.
* Automatically generates an initial palette when the page loads.
* Clean and simple user interface.
* Built entirely with vanilla HTML, CSS, and JavaScript.

## Technologies Used

* **HTML5** — Application structure and UI elements
* **CSS3** — Layout, styling, and visual presentation
* **JavaScript (ES6)** — Random color generation, DOM manipulation, event handling, and clipboard functionality

## Project Structure

```text
Color-Palette-Generator/
│
├── index.html
├── index.js
├── style.css
└── README.md
```

## How It Works

The application generates random HEX color codes using JavaScript.

### 1. Random HEX Color Generation

The application maintains a collection of valid hexadecimal characters:

```javascript
const hex = [
    0, 1, 2, 3, 4, 5, 6, 7, 8, 9,
    "A", "B", "C", "D", "E", "F"
];
```

Six random characters are selected to create a valid HEX color:

```text
#RRGGBB
```

For example:

```text
#3A7FD5
#F2C94C
#8E44AD
#27AE60
```

### 2. Palette Generation

The application generates four random colors for each palette.

```javascript
for (let i = 0; i < 4; i++) {
    colorPalette.push(singleHexColorGenerator());
}
```

### 3. Dynamic Rendering

JavaScript dynamically creates color blocks and applies each generated color as the background:

```javascript
colorDiv.style.background = color;
```

The corresponding HEX value is also displayed inside the color block.

### 4. Copy to Clipboard

When a user clicks on a HEX color value, the application uses the browser Clipboard API to copy the value:

```javascript
navigator.clipboard.writeText(el.innerText);
```

After a successful copy operation, the application displays a confirmation message.

## User Interaction

| Action                    | Result                                    |
| ------------------------- | ----------------------------------------- |
| Open the application      | A random four-color palette is generated  |
| Click **Generate Colors** | A new four-color palette is generated     |
| Click a HEX value         | The color code is copied to the clipboard |

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/KhushiChaubey-493/Color-Palette-Generator.git
```

### 2. Navigate to the Project

```bash
cd Color-Palette-Generator
```

### 3. Run the Application

Open the following file in a modern web browser:

```text
index.html
```

No backend, database, package manager, or external library is required.

## Key JavaScript Concepts Practiced

This project demonstrates practical use of several JavaScript concepts:

* Functions
* Arrow functions
* Arrays
* `Math.random()`
* `Math.floor()`
* Loops
* DOM selection
* Dynamic element creation
* DOM manipulation
* Event listeners
* Template literals
* Browser Clipboard API
* Error handling with Promises

## Learning Objectives

The main objective of this project was to practice building an interactive frontend application using vanilla JavaScript.

Through this project, the following concepts were reinforced:

* Generating random data programmatically
* Dynamically creating HTML elements
* Updating CSS properties using JavaScript
* Handling user interactions
* Working with browser APIs
* Separating HTML, CSS, and JavaScript responsibilities

## Future Improvements

The project can be extended with additional functionality such as:

* Generate palettes with a customizable number of colors.
* Add HEX, RGB, and HSL color formats.
* Add lock/unlock functionality for individual colors.
* Save favorite palettes using `localStorage`.
* Add predefined color harmony modes such as complementary, analogous, and triadic.
* Add a dark/light theme.
* Add gradient generation.
* Add export functionality.
* Add a dedicated color picker.
* Improve accessibility and keyboard navigation.

## Project Status

**Completed — Frontend Practice Project**

The current version focuses on random HEX color generation, dynamic rendering, and clipboard functionality.

## Author

**Khushi Chaubey**

GitHub: https://github.com/KhushiChaubey-493

## License

This project was created for learning and educational purposes.
