# 🎬 YouTube Video Manager (SQLite)

A simple **Python CLI app** to manage YouTube videos using **SQLite** for storage.
You can **add**, **view**, **update**, and **delete** video records.

---

## ⚙️ Requirements

* Python 3.6+
* SQLite (included with Python)

No external libraries needed.

---

## 🚀 How to Run

```bash
python youtube_manager.py
```

*(replace with your script’s filename if different)*

On first run, it creates a `youtube_database.db` file automatically.

---

## 🧩 Features

* 📜 List all saved videos
* ➕ Add new video (title & duration)
* ✏️ Update video info by ID
* ❌ Delete video by ID
* 💾 Auto database creation and persistence

---

## 🧠 Menu Options

```
1. List all videos
2. Add a video
3. Update video details
4. Delete a video
5. Exit
```

Example:

```
Enter your choice (1–5): 2
Enter video title: Python Basics
Enter video duration: 10:45
 Added video 'Python Basics' successfully!
```

---

## 🗃️ Database Table: `videos`

| Column | Type    | Description |
| ------ | ------- | ----------- |
| id     | INTEGER | Primary Key |
| name   | TEXT    | Video Title |
| time   | TEXT    | Duration    |

---

## 🪪 License

MIT License – Free to use and modify.

---
