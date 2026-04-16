# Contributing to Camera Database

Thank you for your interest in contributing! This project welcomes data corrections, new camera entries, translations, and other improvements.

## How to Contribute

### Data Corrections

If you find incorrect camera specifications:

1. Open an issue using the **Data Correction** template
2. Provide the correct value and a reference source
3. Or submit a PR with changes to both `data/camera_data.csv` and `data/camera_data.json`

### Adding New Cameras

To add a new camera to the database:

1. Add a row to `data/camera_data.csv` with all 37 fields
2. Regenerate `data/camera_data.json` to keep both files in sync
3. Add a camera image to `data/images/` following the naming convention: `brand_model-name.png` (lowercase, hyphens for spaces)
4. Submit a PR

### Translations

Documentation is maintained in 6 languages under `doc/`. To improve a translation:

1. Edit the corresponding `doc/README_XX.md` file
2. Keep the structure consistent with other language versions

### Image Contributions

- Format: PNG or JPG
- Naming: `brand_model-name.png/jpg` (all lowercase)
- Place in `data/images/`

## Data Format Requirements

- **CSV and JSON must stay in sync** — any change to one must be reflected in the other
- All 37 columns must be present in every record
- `Brand` and `Model` fields must not be empty
- `Year` should be a valid 4-digit year
- Use `null` (JSON) or empty string (CSV) for missing values

## Commit Messages

This project uses [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` new cameras or features
- `fix:` data corrections
- `docs:` documentation changes
- `chore:` maintenance tasks

## Questions?

Open an issue and we'll be happy to help.
