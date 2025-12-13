*InkShell* — Markdown Meets REPL

*InkShell* is a browser-based Markdown editor with REPL-style code
simulation and file-saving capabilities. It’s designed for developers who
want to write documentation, test code snippets, and kickstart their
projects—all in one elegant interface.
✨ Features

   -

   📝 *Live Markdown Editor* — Write and preview Markdown in real time
   -

   💾 *Save Markdown Files* — Download your content as .md files locally
   -

   🐍 *Python3 REPL Simulation* — Run Python code blocks using Pyodide
   -

   💎 *Ruby IRB-style Prompt* — Simulate Ruby sessions (via optional Opal
   integration)
   -

   🧠 *Start Your Repo from the Browser* — Type code as if you're in python3
    or irb
   -

   🌐 *Frontend-Only or Fullstack* — Use standalone HTML or connect to a
   backend for persistence

🛠 Tech Stack
Layer Technology Purpose
Frontend HTML, CSS, JS Markdown editor + REPL UI
Markdown marked.js Markdown parsing and rendering
Python REPL Pyodide In-browser Python execution
Ruby REPL Opal (optional) Ruby-to-JS transpilation
Backend *Python (FastAPI)* Save/load Markdown files, manage sessions
Storage SQLite / FileSystem Store markdown content and history




# Welcome to InkShell

Start your coding session below:

## Python3

```python
>>> print("Hello from Python3")
Hello from Python3
