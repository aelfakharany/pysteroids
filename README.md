# Pysteroids
Pysteroids is a [Pygame](https://www.pygame.org/wiki/about) implementation of the classic game Asteroids.

## How to Run (assumes nothing is installed)

Prerequisites:

- Python 3.13 or later
- A working `pip` (Python package installer)
- Optional but recommended: `pipx` to install CLI tools in isolated environments

1) Install Python

- macOS / Linux: Install from https://www.python.org/downloads/ or use your OS package manager (Homebrew, apt, etc.).
- Windows: Install from https://www.python.org/downloads/ and enable "Add Python to PATH".

2) (Recommended) Install `pipx` and `uv` so you can run commands isolated from your system Python

```bash
python -m pip install --user pipx
python -m pipx ensurepath
pipx install uv
```

If you prefer not to use `pipx`, you can install `uv` (or skip it) with:

```bash
# install uv for the current Python
python -m pip install --user uv
```

3) Create and activate a virtual environment (optional but recommended)

macOS / Linux:

```bash
python -m venv .venv
source .venv/bin/activate
```

Windows (PowerShell):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

4) Install project dependencies

With `uv` (recommended):

```bash
uv pip install -e .
```

Without `uv` (using pip directly):

```bash
pip install -e .
```

5) Run the game

With `uv`:

```bash
uv run python main.py
```

Or, in an activated virtualenv or system Python:

```bash
python main.py
```

Troubleshooting

- If `pip install` fails when building `pygame`, you may need platform libraries (SDL). See https://www.pygame.org/wiki/GettingStarted for platform-specific instructions.
- If commands like `pipx` or `uv` are not found after installation, restart your terminal or ensure your user-level bin directory is on `PATH`.
- If you run into permission errors, prefer `--user` installs or use a virtual environment rather than `sudo`.