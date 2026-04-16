# Camera Database

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
![Cameras](https://img.shields.io/badge/Cameras-3%2C586-green)
![Brands](https://img.shields.io/badge/Brands-36-orange)
![Images](https://img.shields.io/badge/Images-3%2C546-purple)

An open-source database of camera specifications and images for research and application development.

[![English](https://img.shields.io/badge/English-doc%2FREADME__en.md-blue)](doc/README_en.md) [![中文](https://img.shields.io/badge/中文-doc%2FREADME__zh.md-red)](doc/README_zh.md) [![日本語](https://img.shields.io/badge/日本語-doc%2FREADME__ja.md-green)](doc/README_ja.md) [![Español](https://img.shields.io/badge/Español-doc%2FREADME__es.md-yellow)](doc/README_es.md) [![Français](https://img.shields.io/badge/Français-doc%2FREADME__fr.md-purple)](doc/README_fr.md) [![Deutsch](https://img.shields.io/badge/Deutsch-doc%2FREADME__de.md-orange)](doc/README_de.md)

## Overview

This repository contains detailed specifications for **3,860 digital cameras** from **36 manufacturers**, with **3,858 product images**.

**Camera Brands**: Acer, AgfaPhoto, BenQ, Canon, Casio, Concord, Contax, Epson, Fujifilm, GE, HP, JVC, Jenoptik, Kodak, Konica, Konica-Minolta, Kyocera, Leica, Minolta, Minox, Nikon, Nokia, Olympus, Panasonic, Pentax, Praktica, Ricoh, Rollei, Samsung, Sanyo, Sigma, Sony, Toshiba, Vivitar, Yakumo, Zeiss

## Quick Start

### Python

```python
import pandas as pd

df = pd.read_csv("data/camera_data.csv")

# Filter by brand
canon = df[df["Brand"] == "Canon"]
print(f"Canon cameras: {len(canon)}")

# Find full-frame cameras (crop factor = 1.0)
ff = df[df["Crop factor"] == "1.0"]
print(f"Full-frame cameras: {len(ff)}")
```

### JavaScript

```javascript
const fs = require("fs");

const cameras = JSON.parse(fs.readFileSync("data/camera_data.json", "utf8"));

// Filter by brand
const sony = cameras.filter((c) => c.Brand === "Sony");
console.log(`Sony cameras: ${sony.length}`);
```

## Data Files

| File | Format | Description |
|------|--------|-------------|
| `data/camera_data.csv` | CSV | 3,860 cameras, 37 columns |
| `data/camera_data.json` | JSON | Same data in structured format |
| `data/images/` | PNG/JPG | 3,858 product images |

## Data Structure

Each camera record contains 37 fields:

| Field | Description |
|-------|-------------|
| Brand | Manufacturer |
| Model | Model name |
| Year | Release year |
| image_file | Path to product image |
| Total megapixels | Total megapixels |
| Sensor resolution | Resolution (width x height) |
| Sensor type | CCD, CMOS, etc. |
| Sensor size | Physical sensor dimensions (mm) |
| Crop factor | Sensor crop factor |
| Max aperture | Maximum aperture |
| Focal length (35mm equiv.) | 35mm equivalent focal length |
| Max. shutter speed | Fastest shutter speed |
| Min. shutter speed | Slowest shutter speed |
| ISO | ISO sensitivity range |
| Max. image resolution | Maximum image resolution |
| Max. video resolution | Maximum video resolution |
| Screen size | LCD screen size (inches) |
| Screen resolution | LCD resolution (dots) |
| Viewfinder | Viewfinder type |
| Metering | Metering modes |
| Aperture priority | Aperture priority mode |
| Shutter priority | Shutter priority mode |
| Exposure Compensation | Exposure compensation range |
| White balance presets | White balance presets count |
| Normal focus range | Regular focus distance |
| Macro focus range | Macro focus distance |
| Optical zoom | Optical zoom support |
| Digital zoom | Digital zoom support |
| Storage types | Compatible storage media |
| Battery | Battery type |
| USB | USB interface type |
| Weight | Weight (g) |
| Dimensions | Physical dimensions (mm) |
| Effective megapixels | Effective megapixels |
| Megapixels | Marketing megapixel count |
| Max. aperture (35mm equiv.) | 35mm equivalent max aperture |
| Also known as | Alternative model names |

## Image Data

- **Format**: PNG and JPG
- **Naming**: `brand_model-name.png/jpg` (lowercase)
- **Coverage**: 36 manufacturers, 3,858 images

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on submitting data corrections, new cameras, translations, and more.

## License

[MIT License](LICENSE) - free for commercial and non-commercial use.
