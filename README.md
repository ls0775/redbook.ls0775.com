# Redbook Pricing & Specification Scraper

A utility for collecting and managing automotive pricing and technical specification data from Redbook.com.au. This project provides synthesized datasets for specific luxury and 4WD models, along with a Python-based scraper template for future data extraction.

## 🚀 Features

- **Multi-Year Data:** Comprehensive year-by-year pricing for all relevant series (80, 100, 200, and 300 where applicable).
- **Badge Specificity:** Detailed data for specific trim levels including GXL, VX, Sahara, Sports Luxury, and "S" variants.
- **Deep Technical Specs:** Captures engine codes, power, torque, transmission types, and gear counts.
- **Market Valuation:** Includes original MSRP ("Price when New"), Private Sale ("I'm Selling"), and Dealer Trade-in ("I'm Trading") ranges.

## 📊 Data Structure (CSV Columns)

All generated CSV files follow a standardized format:

| Column | Description |
| :--- | :--- |
| `Year` | Model year of the vehicle |
| `Make` | Manufacturer (e.g., Toyota, Lexus) |
| `Model` | Vehicle model (e.g., Landcruiser, LX570) |
| `Badge` | Trim level or series (e.g., Sahara, GXL) |
| `Price when New` | Original Recommended Retail Price (RRP) |
| `I'm Selling` | Estimated Private Sale price range |
| `I'm Trading` | Estimated Dealer Trade-in price range |
| `Engine Size (L)` | Displacement in Litres |
| `Engine Size (cc)` | Displacement in Cubic Centimeters |
| `Engine Code` | Specific engine identifier (e.g., 1UR-FE, 3UR-FE) |
| `Power (kW)` | Maximum power output |
| `Torque (Nm)` | Maximum torque output |
| `Fuel Type` | Specific fuel requirements (e.g., Petrol - Unleaded ULP) |
| `Transmission` | Transmission type (Automatic/Manual) |
| `Number of Gears` | Count of forward gears |

## 📁 Output Directory

All synthesized datasets are stored in the `/outputs` folder:
- `outputs/lexus_lx570_pricing.csv`: Data from 2008–2021.
- `outputs/toyota_landcruiser_pricing.csv`: Petrol ULP data from 1992–2019 (GXL, VX, Sahara).

## 🛠 Usage

### Scraper Script
The `scraper.py` script serves as a template for future programmatic queries.

```bash
# Basic usage
python scraper.py --make "Toyota" --model "Landcruiser"

# Help
python scraper.py --help
```

*Note: Production-grade scraping from Redbook.com.au requires browser automation (e.g., Playwright/Selenium) to handle DataDome and Captcha protections.*

## 📝 Configuration
Project mandates and detailed developer instructions can be found in `GEMINI.md`.
