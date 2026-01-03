## Getting Started

- **Download VS Code**  
Download and install Visual Studio Code from: https://code.visualstudio.com/download

- **Create your HTML file**  
Create a new file called `website.html`, then copy and paste the following contents into it:

```html
<!DOCTYPE html>
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
Add the following style block in between the `</body>` and `</html>` tags of your `website.html` file:

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
</style>
```

- **Add Class & ID targeted Styling**  
Add the following style definitions **inside** the bottom of the `<style>` block in `website.html`, directly under the `.section-content` definition:

```css
/* Class & ID targeted styling */
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
Add the following `<script>` in between the `</style>` and `</html>` tags of your `website.html` file:

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
