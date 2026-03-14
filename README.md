# Core Usage

Repository containing `pixelsurvey-core` as a submodule and specific recipes.

## Structure

```
core-usage/
├── pixelsurvey-core/    (Git submodule)
├── recipes/             (Your recipe files)
└── run.py              (Script to run surveys)
```

## Initial Setup

1. **Clone the repo with submodules:**
```bash
git clone --recursive https://github.com/your-org/core-usage.git
cd core-usage
```

2. **If you already cloned without submodules:**
```bash
git submodule update --init --recursive
```

## Usage

```bash
# Run from the core-usage folder
python run.py safe-seoul-pilot-en-v1_3
```

## Notes on Paths

- `recipes/` in core-usage points to `PROJECT_ROOT/recipes` in `vars.py`
- `surveys/` is generated in `PROJECT_ROOT/surveys` in `vars.py`
- All paths are relative and work correctly

## Update pixelsurvey-core

```bash
cd pixelsurvey-core
git pull origin main  # or the branch you use
cd ..
git add pixelsurvey-core
git commit -m "Update pixelsurvey-core submodule"
```
