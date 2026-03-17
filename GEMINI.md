# Redbook Scraper

This project is a utility to scrape car pricing and specification data from Redbook.com.au and export it to a CSV file.

## Project Overview
The scraper targets specific car makes and models, iterating through all available years to collect pricing guides and technical specifications.

## Data Requirements
For each vehicle entry, the following columns are captured:
- **Vehicle Identity:** Year, Make, Model, Badge.
- **Pricing:**
    - `Price when New`
    - `I'm Selling` (Private Price Guide range)
    - `I'm Trading` (Trade-in price guide range)
- **Specifications:**
    - `Engine Size (cc)`
    - `Engine Size (L)`
    - `Engine Code`
    - `Power`
    - `Torque`
    - `Fuel Type` (e.g., Petrol - Unleaded ULP)
    - `Transmission` (e.g., Automatic, Manual)
    - `Number of Gears` (e.g., 5, 6, 8)

## Usage
### Running the Scraper
To generate a CSV for a specific model (e.g., Lexus LX570), run the scraper script with the desired make and model as inputs.

```bash
# Example (once script is implemented)
python scraper.py --make "Lexus" --model "LX570"
```

## Development Conventions
- **Language:** Python
- **Output Format:** CSV (`lexus_lx570_pricing.csv` by default for the test case)
- **Reliability:** The scraper handles pagination and navigates to individual specification pages for deep data extraction.
