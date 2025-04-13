# 📝 AI Sticky Notes

AI Sticky Notes is a lightweight tool built using the `FastMCP` framework that allows users to add, read, and summarize notes. It stores all notes in a local `notes.txt` file and provides an interactive interface via MCP tools and resources.

## 🚀 Features

- Add sticky notes with a simple message
- Read all saved notes at once
- Get the most recently added note
- Generate a summary prompt based on all current notes

## 📁 Project Structure

```
project_mcp/
│
├── main.py           # Entry point for the FastMCP server
├── notes.txt         # File used to persist sticky notes
└── README.md         # Project documentation
```

## 🛠️ Installation

Make sure you have Python 3.10+ installed.

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/project_mcp.git
   cd project_mcp
   ```

2. **Create and activate a virtual environment**
   ```bash
   python -m venv .venv
   .venv\Scripts\activate  # Windows
   ```

3. **Install dependencies using [uv](https://github.com/astral-sh/uv)**
   ```bash
   uv pip install fastmcp
   ```

## 📌 Usage

Run the server using `uv`:

```bash
uv run python main.py
```

This will start the `FastMCP` server with the name **"AI Sticky Notes"**.

## 🧰 Available Tools & Resources

### Tools

- `add_note(message: str)`  
  Adds a new note to the file.

- `read_notes()`  
  Reads and returns all stored notes.

### Resources

- `notes://latest`  
  Returns the most recently added note.

### Prompts

- `note_summary_prompt()`  
  Returns a prompt string asking an AI to summarize the current notes.

## 📄 Example

```python
add_note("Buy groceries")
read_notes()  # → "Buy groceries"
get_latest_note()  # → "Buy groceries"
note_summary_prompt()  # → "Summarize the current notes: Buy groceries"
```

## 💡 Future Ideas

- Add timestamps to notes
- Tag notes by category
- Implement deletion or editing
- Build a simple web frontend using Streamlit or FastAPI

---

Made with 💬 and Python using [FastMCP](https://github.com/astral-sh/fastmcp)

