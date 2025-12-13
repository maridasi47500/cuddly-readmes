<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Markdown Editor</title>
  <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
  <style>
    body {
      font-family: Arial, sans-serif;
      display: flex;
      gap: 20px;
      padding: 20px;
    }
    textarea {
      width: 50%;
      height: 90vh;
      font-family: monospace;
      font-size: 16px;
      padding: 10px;
    }
    #preview {
      width: 50%;
      height: 90vh;
      overflow-y: auto;
      border-left: 1px solid #ccc;
      padding: 10px;
      background: #f9f9f9;
    }
    h1, h2, h3 { margin-top: 0; }
  </style>
</head>
<body>
  <textarea id="markdown" oninput="updatePreview()">
# Welcome to the Markdown Editor!

Type your Markdown on the left, and see the preview on the right.

## Features
- Live preview
- GitHub-flavored Markdown
- Easy to customize

**Enjoy writing!**
  </textarea>

  <div id="preview"></div>

  <script>
    function updatePreview() {
      const markdownText = document.getElementById("markdown").value;
      document.getElementById("preview").innerHTML =
marked.parse(markdownText);
    }

    // Initial render
    updatePreview();
  </script>
</body>
</html>
