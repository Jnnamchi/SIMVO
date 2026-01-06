## Getting Started

- **Download VS Code**  
Download and install Visual Studio Code from: https://code.visualstudio.com/download

## Website Development

- **Create your HTML file**  
Create a new file called `website.html`, then copy and paste the following contents into it:

```html
<html>

<head>
  <title>John's Website</title>
</head>

<body>
  <div class="section" id="title">
    <div class="section-content">
      <h1>John's Website</h1>
      <button>Click for action</button>
    </div>
  </div>
</body>

</html>
```

- **Add Core Element Styling**  
Add the following `<style>` block in between the `</body>` and `</html>` tags of your `website.html` file:

```html
<style>
  html, body {
    margin: 0;
    padding: 0;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
  }

  button {
    margin-top: 16px;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    border-radius: 15px;
  }
</style>
```

- **Add Class & ID targeted Styling**  
Add the following style definitions **inside** the bottom of the `<style>` block in `website.html`, directly under the `.section-content` definition:

```css
/* Class & ID targeted styling */
.section {
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.section-content {
  text-align: center;
}

#title {
  color: white;
  background:
    radial-gradient(circle at top left, #ff6ec4, transparent 50%),
    radial-gradient(circle at top right, #7873f5, transparent 50%),
    radial-gradient(circle at bottom left, #42e695, transparent 50%),
    radial-gradient(circle at bottom right, #fddb92, transparent 50%),
    linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d);
}

#title button {
  border: solid white 1px;
  color: white;
  background: none;
  transition: background-color 0.3s ease, color 0.3s ease;
}

#title button:hover {
  background-color: white;
  color: #b21f1f;
}
```

- **Add JavaScript**  
Add the following `<script>` block in between the `</style>` and `</html>` tags of your `website.html` file:

```html
<script>
  function generateRandomBackground() {
    message = "Hello!"
    alert(message)
  }
</script>
```

Also add the following `onclick` attribute to the `<button>` element so it now looks like:
```html
<button onclick="generateRandomBackground()">Click for action</button>
```

- **Make the JS Function Useful**  
Replace the entire contents of the `<script>` block with the following functions. (Do not delete `<script>` tags):

```js
// Helper to generate a random hex color
function randomColor() {
  return `#${Math.floor(Math.random() * 16777215)
    .toString(16)
    .padStart(6, '0')}`;
}

// Generate a randomized gradient background
function generateRandomBackground() {
  const c1 = randomColor();
  const c2 = randomColor();
  const c3 = randomColor();
  const c4 = randomColor();
  const c5 = randomColor();
  const c6 = randomColor();
  const c7 = randomColor();

  const title = document.getElementById('title');
  title.style.background = `
    radial-gradient(circle at top left, ${c1}, transparent 50%),
    radial-gradient(circle at top right, ${c2}, transparent 50%),
    radial-gradient(circle at bottom left, ${c3}, transparent 50%),
    radial-gradient(circle at bottom right, ${c4}, transparent 50%),
    linear-gradient(135deg, ${c5}, ${c6}, ${c7})
  `;
}
```

- **Run the JS Function on Page Load**  
Add the `generateRandomBackground` function call **inside** the bottom of the `<script>` block in `website.html`:

```js
generateRandomBackground()
```

## Network Requests

- **Select an API**  
Select one of the following APIs of your interest:

- Random Facts: https://uselessfacts.jsph.pl/api/v2/facts/random
- Random Excuses: https://excuser-three.vercel.app/v1/excuse
- Random Quotes: https://zenquotes.io/api/random
- Random Bible Verses: https://bible-api.com/data/web/random
- Random Dog Facts: https://dogapi.dog/api/facts?number=1
- Random Cat Facts: https://meowfacts.herokuapp.com/
- Random Pictures of Food: https://foodish-api.com/api/
- Random Startup Idea Generator: https://itsthisforthat.com/api.php?json
- Get Current BitCoin Price: https://api.coinpaprika.com/v1/tickers/btc-bitcoin
