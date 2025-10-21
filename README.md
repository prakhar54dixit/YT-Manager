
# YT-Manager

A small, easy-to-use command-line YouTube video manager that stores video metadata (title and duration) in a local SQLite database. This project is intentionally minimal and perfect for learning CRUD operations with SQLite in Python or for quick personal use.

## Features

- List all videos
- Add a video (title + duration)
- Update a video's title and duration
- Delete a video
- Stores data in `youtube_database.db` (SQLite)

## Requirements

- Python 3.8+ (SQLite3 comes bundled with the standard library)

## Installation

1. Clone the repository:

	git clone https://github.com/ansh1406/YT-Manager.git
	cd YT-Manager

2. (Optional) Create and activate a virtual environment:

	# Windows (PowerShell)
	python -m venv .venv; .\.venv\Scripts\Activate.ps1

3. No external dependencies are required — the script uses Python's builtin `sqlite3`.

## Usage

Run the script with Python. It will create `youtube_database.db` in the current directory on first run.

# Windows (PowerShell)
python .\yt_manager_db.py

Follow the interactive numbered menu to list, add, update, or delete videos.

## Database details

The script creates a single table named `videos` with the following schema:

- id INTEGER PRIMARY KEY AUTOINCREMENT
- name TEXT NOT NULL
- time TEXT NOT NULL

You can open `youtube_database.db` with any SQLite client to inspect or back up your data.

## Contract (quick)

- Inputs: user selects menu choices (1-5) and provides text for titles/duration or numeric IDs when prompted.
- Outputs: console-printed lists and confirmation messages; a local SQLite database file is updated.
- Error modes: invalid numeric input (handled with prompts), missing video id (prints a message); disk permission errors will raise exceptions.

## Edge cases

- Empty database: the list command prints a friendly message.
- Non-numeric IDs or menu choices: the script catches ValueError and prompts again.
- Concurrent writes: SQLite supports concurrent readers but serializes writers — avoid running multiple writers at the same time.

## Development

- Suggested improvements:
  - Add unit tests around DB operations.
  - Add argument flags to perform non-interactive operations (for scripting).
  - Add export/import (CSV/JSON) features.

## Contributing

Contributions are welcome. Please open issues or submit pull requests. Keep changes small and include tests where appropriate.

## License

This repository does not include a license file by default. If you'd like to license this project, add a `LICENSE` (for example MIT) and update this section.

## Contact

GitHub: https://github.com/ansh1406

---
Small, focused CLI for managing video metadata — simple, educational, and ready for extensions.

