# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dynamic Interaction with JavaScript</title>
  
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .highlight {
            color: blue;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <header>
        <h1 id="title">Welcome to My Interactive Page</h1>
    </header>

    <main>
        <article>
            <p id="description">This is a simple example demonstrating JavaScript interactivity.</p>
        </article>
        
        <section>
            <button id="change-text-btn">Change Text</button>
            <button id="toggle-element-btn">Add/Remove Element</button>
        </section>

        <div id="element-container"></div>
    </main>

    <footer>
        <p>Enjoy experimenting with JavaScript!</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
javascript file.
// Change text content dynamically
document.getElementById("change-text-btn").addEventListener("click", () => {
    const title = document.getElementById("title");
    const description = document.getElementById("description");

    // Change text and style
    title.textContent = "Text Changed Dynamically!";
    title.classList.add("highlight");
    description.textContent = "The text content of this page has been updated via JavaScript.";
});

// Add/Remove an element
document.getElementById("toggle-element-btn").addEventListener("click", () => {
    const container = document.getElementById("element-container");
    const existingElement = document.getElementById("dynamic-element");

    if (existingElement) {
        container.removeChild(existingElement); // Remove element
    } else {
        const newElement = document.createElement("div");
        newElement.id = "dynamic-element";
        newElement.textContent = "I'm a dynamically added element!";
        container.appendChild(newElement); // Add element
    }
});
