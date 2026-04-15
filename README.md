# Color Palette Project

## Aim

To design and develop a simple web application that allows users to dynamically change the text color and background color using interactive color picker tools.

## Procedure

1. Create a project folder and initialize it using Git.
2. Create an `index.html` file in the project directory.
3. Design the webpage structure using HTML elements such as headings, inputs, buttons, and paragraph.
4. Use `<input type="color">` to provide color selection bars for user interaction.
5. Apply CSS styles to enhance the appearance of the webpage.
6. Use JavaScript to:

   - Capture selected color values
   - Apply selected color to text
   - Apply selected color to background
   - Reset colors to default values
7. Test the application in a browser.
8. Push the project to GitHub.

## Code

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Color Palette Project</title>

  <style>
    body {
      font-family: "Segoe UI", Arial, sans-serif;
      text-align: center;
      background-color: #f0f0f0;
      transition: background-color 0.3s ease;
    }

    h2 {
      font-size: 32px;
      margin-top: 20px;
    }

    .box {
      margin: 15px;
    }

    input[type="color"] {
      width: 60px;
      height: 40px;
      border: none;
      cursor: pointer;
    }

    p {
      font-size: 28px;
      margin-top: 30px;
      color: #222;
      transition: color 0.3s ease;
    }

    button {
      padding: 10px 20px;
      cursor: pointer;
      border: none;
      background-color: #444;
      color: white;
      border-radius: 6px;
    }
  </style>
</head>

<body>

  <h2>Color Palette Project</h2>

  <div class="box">
    <label>Text Color:</label>
    <input type="color" id="textColorPicker" onchange="changeTextColor()">
  </div>

  <div class="box">
    <label>Background Color:</label>
    <input type="color" id="bgColorPicker" onchange="changeBackgroundColor()">
  </div>

  <button onclick="resetColors()">Reset</button>

  <p id="unity">Prasanna Tejaswi</p>

  <script>
    function changeTextColor() {
      let color = document.getElementById("textColorPicker").value;
      document.getElementById("unity").style.color = color;
    }

    function changeBackgroundColor() {
      let color = document.getElementById("bgColorPicker").value;
      document.body.style.backgroundColor = color;
    }

    function resetColors() {
      document.getElementById("unity").style.color = "#222";
      document.body.style.backgroundColor = "#f0f0f0";
    }
  </script>

</body>
</html>

## Output

A webpage is displayed with:

  - Color picker for text color
  -Color picker for background color
  - A sample text: **"Prasanna Tejaswi"
 When user selects a color:
  -Text color changes instantly
  - Background color updates dynamically
  -Reset button restores default colors

## Result

The color palette web application was successfully created.
Users can interactively change text and background colors using color pickers, demonstrating basic HTML, CSS, and JavaScript DOM manipulation.


