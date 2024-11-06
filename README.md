# InputBox

## Overview
This project provides a customizable, lightweight, and responsive input-box component. The component is styled using CSS variables to allow quick adjustments to theme colors, text styles, and transitions. It includes customizable alignment, error states, and various sizes.

## Features
- **Input-Box Component**: A reusable input box with options for styling and alignment.
- **Error State**: Easily displays error styling and messages.
- **Modular and Flexible**: Multiple modifier classes (`mod_small`, `mod_alignRight`, `mod_uppercase`) to tailor the component’s appearance.
- **Themeable**: Customize colors, font, and transition duration using CSS variables.

## Installation
1. Clone the repository:
    ```bash
    git clone <repository-link>
    ```
2. Navigate to the project directory and include `main.js` and `main.css` in your project.

## Usage
1. Import the CSS and JS files in your HTML:
    ```html
    <link rel="stylesheet" href="path/to/main.css">
    <script src="path/to/main.js"></script>
    ```
2. Use the `<input-box>` custom component in your HTML:
    ```html
    <input-box class="mod_alignRight mod_uppercase">
        <div class="title">
            <span class="titleElem">Title</span>
            <span class="errorElem">Error message</span>
        </div>
        <div class="body">
            <input type="text" class="input" placeholder="Enter text...">
            <div class="icon">Icon</div>
        </div>
    </input-box>
    ```

### JavaScript Initialization Example
To initialize and control the input box with JavaScript:
```javascript
// Assuming main.js exports a class or function to initialize the input-box

// Example: Initialize the input-box with custom settings
document.addEventListener("DOMContentLoaded", () => {
    // Select the input-box element
    const inputBox = document.querySelector("input-box");

    // Initialize it with any options if main.js provides a setup function
    const initializedInputBox = new InputBox(inputBox, {
        placeholder: "Type here...",
        showError: false,
    });

    // You can then access or manipulate it via JavaScript
    initializedInputBox.setError("Please enter a valid value"); // Show an error message
    initializedInputBox.clearError(); // Clear the error message
});
