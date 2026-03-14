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

2. **Create a Python venv with the rquirements**
```bash
python -m venv .psenv
.psenv/bin/actiavte
pip install -r requirements.txt
```

## Usage

```bash
# Run from the core-usage folder
cd core-usage
python -m pixelsurvey_core.survey_gen <survey_id>

# Example:
python -m pixelsurvey_core.survey_gen homes-example
```

## How it Works

- Recipe files go in `core-usage/recipes/`
- Generated surveys are created in `core-usage/surveys/`
- Both paths are configured automatically via `vars.py` in `pixelsurvey-core`
- The submodule ensures you always have the correct version of the generator
