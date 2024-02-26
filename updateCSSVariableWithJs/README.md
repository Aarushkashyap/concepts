## Scoped CSS Variables and JS

This project demonstrates how to manipulate CSS variables using JavaScript, allowing real-time adjustments to the visual appearance of an image.

### Functionality:

- **Interactive Controls:** Sliders and a color picker control the spacing, blur effect, and base color of an image, providing a visually engaging experience.
- **Live Updates:** Changes made to the controls are instantly reflected on the image, offering immediate feedback and a dynamic visual experience.
- **Scoped Variables:** The use of `:root` ensures that variable changes are scoped to the entire document, preventing unintended modifications to other elements.

### Technical Details:

- HTML: Structures the layout and includes the image element.
- CSS: Defines initial values for the CSS variables and styles the page elements.
  - `:root`: Contains the initial definitions of `--base`, `--spacing`, and `--blur` variables.
  - `img`: Leverages the defined variables for padding, background color, and blur filter.
  - `.hl`: Applies the `--base` color to highlight the "JS" text using scoped variables.
- JavaScript:
  - Selects all input elements within the `.controls` class using `querySelectorAll`.
  - Defines the `handleUpdate` function to:
    - Retrieve the data-sizing attribute (if present) to add appropriate units (px, etc.) to the value.
    - Set the corresponding CSS variable (`--${this.name}`) using `document.documentElement.style.setProperty` with the updated value.
  - Attaches both `change` and `mousemove` event listeners to each input element, triggering the `handleUpdate` function on user interaction.

### Usage:

1. Open the `index.html` file in your web browser once you have cloned the files .
2. Use the sliders and color picker to adjust the spacing, blur, and base color of the image.
3. Observe the real-time changes applied to the image, demonstrating the dynamic nature of CSS variables controlled by JavaScript.

### Customization:

- Modify the CSS styles to adjust the initial appearance of the image and its container.
- Replace the image source with your own image file.
- Experiment with different CSS variables to explore their potential for controlling various visual aspects.
