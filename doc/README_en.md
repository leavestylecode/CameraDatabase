# Camera Database

An open-source database of camera specifications and images for research and application development.

## Overview

This repository contains detailed specifications for 3,794 digital cameras from various manufacturers.



## Repository Structure

```
CameraDatabase/
├── data/                          # Data directory
│   ├── camera_data.csv    # CSV format camera specifications
│   ├── camera_data.json   # JSON format camera specifications
│   └── images/            # Camera images organized by brand
├── doc/                           # Documentation directory
│   ├── README_en.md               # English documentation (this file)
│   ├── README_zh.md               # Chinese documentation
│   ├── README_ja.md               # Japanese documentation
│   ├── README_es.md               # Spanish documentation
│   ├── README_fr.md               # French documentation
│   └── README_de.md               # German documentation
├── CHANGELOG.md                   # Project changelog
└── README.md                      # Main README
```




## Data Files

- `data/camera_data.csv`: CSV format camera specifications (37 columns)
- `data/camera_data.json`: JSON format camera specifications (same data as CSV)
- `data/images/`: Camera images organized by brand and model (3,546 images)

## Data Structure

The dataset includes the following fields:

| Field | Description |
|-------|-------------|
| Brand | Camera manufacturer |
| Model | Camera model name |
| Year | Release year |
| image_file | Path to the camera image |
| Total megapixels | Total number of megapixels |
| Exposure Compensation | Available exposure compensation range |
| Normal focus range | Regular focusing distance range |
| Battery | Battery type |
| Sensor resolution | Resolution in pixels (width x height) |
| Crop factor | Sensor crop factor |
| Sensor type | Type of image sensor (CCD, CMOS, etc.) |
| Dimensions | Physical dimensions (mm) |
| Max aperture | Maximum aperture value |
| Min. shutter speed | Minimum shutter speed |
| White balance presets | Number of white balance presets |
| Macro focus range | Minimum focusing distance for macro photography |
| Optical zoom | Whether optical zoom is available |
| USB | USB interface type |
| Weight | Camera weight (g) |
| Max. aperture (35mm equiv.) | Maximum aperture in 35mm equivalent |
| Focal length (35mm equiv.) | Focal length range in 35mm equivalent |
| Also known as | Alternative names or models |
| Aperture priority | Whether aperture priority mode is available |
| Max. image resolution | Maximum image resolution in pixels |
| Max. shutter speed | Maximum shutter speed |
| Storage types | Compatible storage media |
| Effective megapixels | Effective megapixels used for image capture |
| Megapixels | Marketing megapixel count |
| Max. video resolution | Maximum video resolution |
| Screen size | LCD screen size in inches |
| Metering | Available metering modes |
| Digital zoom | Whether digital zoom is available |
| Shutter priority | Whether shutter priority mode is available |
| Sensor size | Physical sensor dimensions (mm) |
| Viewfinder | Viewfinder type |
| Screen resolution | LCD screen resolution in dots |
| ISO | Available ISO sensitivity range |

## Image Data

The database includes 3,546 camera images organized by brand and model:

- **Format**: PNG and JPG files
- **Naming Convention**: `brand_model-name.png/jpg`
- **Organization**: Images are stored in `data/images/` directory
- **Coverage**: All 36 camera manufacturers have image representation
- **Quality**: High-quality product images suitable for research and applications

## Data Format

The data is available in two formats:

1. **CSV**: Simple tabular format suitable for spreadsheet applications and data analysis tools
2. **JSON**: Structured format ideal for web applications and programming

### JSON Example

```json
{
    "Brand": "Canon",
    "Model": "EOS R5 Mark II",
    "Year": "2024",
    "image_file": "data/images/canon_eos-r5-mark-ii.jpg",
    "Total megapixels": "50.3",
    "Exposure Compensation": "\u00b13 EV (in 1/3 EV, 1/2 EV steps)",
    "Normal focus range": null,
    "Battery": "LP-E6P lithium-ion battery",
    "Sensor resolution": "8216 x 5477",
    "Crop factor": "1.0",
    "Sensor type": "CMOS",
    "Dimensions": "138.5 x 101.2 x 93.5 mm",
    "Max aperture": null,
    "Min. shutter speed": "30 sec",
    "White balance presets": "8.0",
    "Macro focus range": null,
    "Optical zoom": null,
    "USB": "USB 3.2 (10 GBit/sec)",
    "Weight": "746 g",
    "Max. aperture (35mm equiv.)": null,
    "Focal length (35mm equiv.)": null,
    "Also known as": null,
    "Aperture priority": "Yes",
    "Max. image resolution": "8192 x 5464",
    "Max. shutter speed": "1/8000 sec",
    "Storage types": "SD/SDHC/SDXC, CFexpress Type B",
    "Effective megapixels": "45.0",
    "Megapixels": null,
    "Max. video resolution": "8192x4320 (60/50/30p/\u200b25p/24p)",
    "Screen size": "3.2\"",
    "Metering": "Multi, Center-weighted, Spot, Partial",
    "Digital zoom": null,
    "Shutter priority": "Yes",
    "Sensor size": "36 x 24 mm",
    "Viewfinder": "Electronic",
    "Screen resolution": "2,100,000 dots",
    "ISO": "Auto, 100-51200 (extends to 50-102400)"
  }
```

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

## Usage

This dataset can be used for:

- Camera market analysis
- Computer vision research
- Machine learning model training
- Camera recommendation systems
- Image recognition and classification
- Visual search applications
- Educational purposes
- Product catalog development

## Data Cleaning

The data has been cleaned to:
- Remove empty columns
- Standardize column names
- Sort by brand and release year (descending)
- Convert all missing values to null in JSON format

## License

This dataset is released under the MIT License. Feel free to use it for commercial and non-commercial purposes.

## Contributing

Contributions to improve the dataset are welcome. Please submit a pull request or open an issue to discuss your ideas.

## Acknowledgments

Thanks to all the camera manufacturers and review websites that made the original specifications available. 
