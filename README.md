## Development Setup

### Prerequisites
- Python 3.8 or higher
- Git
- GitHub account
- uv (fast Python package installer) - [Installation guide](https://github.com/astral-sh/uv#installation)

### Step 1: Clone the Repository
```bash
git clone https://github.com/huatoanduong/huatoanduong.github.io.git
cd huatoanduong.github.io
```

### Step 2: Install uv (if not already installed)
```bash
# macOS/Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows (PowerShell)
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"

# Or using pip
pip install uv
```

### Step 3: Create Virtual Environment and Install Dependencies
```bash
# uv will automatically create .venv and install dependencies
uv pip install -r requirements.txt
```

### Step 4: Activate Virtual Environment
```bash
# Windows
.venv\Scripts\activate

# macOS/Linux
source .venv/bin/activate
```

### Step 5: Verify Installation
```bash
mkdocs --version
```

## Local Development

### Serve Locally
```bash
# Make sure virtual environment is activated
# If using uv, you can also run directly:
uv run mkdocs serve

# Or activate the environment first
source .venv/bin/activate  # macOS/Linux
# .venv\Scripts\activate   # Windows
mkdocs serve
```
The site will be available at `http://127.0.0.1:8000/` (or the port specified in `mkdocs.yml`)

### Build for Production
```bash
# Using uv directly
uv run mkdocs build

# Or with activated environment
mkdocs build
```
This creates a `dist/` directory with the built website.

### Clean Build
```bash
mkdocs build --clean
```
Removes the `dist/` directory before building.

## Content Management