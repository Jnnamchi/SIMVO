## Getting Started

- **Download VS Code**  
  Download and install Visual Studio Code from:  
  https://code.visualstudio.com/download

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

- **Add Basic Styling**  
  Copy & place the following style block in between the `</body>` and `</html>` tags of your `website.html` file:

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