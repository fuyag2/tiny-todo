# tiny-todo

A lightweight, offline-first task manager for people who hate task managers.

```
< 5 MB   ~0% CPU   0 trackers   100% offline
```

---

## what it is

Tiny To-do is a minimal desktop task manager built with Python and tkinter. No Electron. No cloud sync. No subscription. It opens in under a second, saves to a plain JSON file, and stays out of your way.

---

## features

- **Priority sorting** — high / medium / low, auto-sorted, color-coded
- **Inline editing** — click any task to edit in place, no dialogs
- **Customize Priority mode** — per-task priority dropdowns on demand
- **Auto-save** — debounced writes to `tasks.json`, 400ms after any change
- **Canvas rendering** — smooth scrolling with zero widget overhead
- **Clear Completed** — wipe all done tasks in one click
- **Resizable** — works from 300×350 to full-screen

---

## install

**Windows** — download `TinyTodo-Windows.exe` from [Releases](../../releases)

**macOS** — download `TinyTodo-macOS.dmg` from [Releases](../../releases)

**From source:**

```bash
pip install customtkinter
python main.py
```

> Requires Python 3.10+

---

## usage

1. Type a task in the input field, pick a priority, press `Enter`
2. Click any task title to edit inline — `Enter` to save, `Esc` to cancel
3. Toggle **Customize Priority** to change priority per task
4. Check the checkbox to complete — tasks auto-sort to the bottom
5. **Clear Completed** removes all done tasks at once

Tasks are saved to `tasks.json` in the app directory — plain text, always readable.

---

## data

```json
[
  { "title": "Review proposal", "done": false, "priority": "high" },
  { "title": "Send report",     "done": false, "priority": "medium" },
  { "title": "Read docs",       "done": true,  "priority": "low"  }
]
```

---

## stack

| | |
|---|---|
| Language | Python 3.10+ |
| UI | tkinter + CustomTkinter |
| Rendering | `tk.Canvas` (custom) |
| Storage | JSON (local file) |
| Packaging | PyInstaller |

---

## license

Free software. Do whatever you want with it.
