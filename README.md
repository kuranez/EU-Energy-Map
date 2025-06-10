# EU Energy Map

An interactive dashboard that visualizes Eurostat data on renewable energy developments across European countries. Built with Python and Panel, the web app provides an intuitive interface to explore renewable energy trends from 2004 to 2022.

## 🌐 Web App

> 🟢 **[Live Demo Coming Soon]**

## Screenshot

> ![https://raw.githubusercontent.com/kuranez/EU-Energy-Map/refs/heads/main/extra/images/screenshots/app.png](https://raw.githubusercontent.com/kuranez/EU-Energy-Map/refs/heads/main/extra/images/screenshots/app.png)

---

## ⚙️ Features

- Interactive dashboard powered by **Panel** and **Plotly**
    
- Time-series visualization of renewable energy shares by country and category
    
- Geospatial mapping using **GeoJSON** and **GeoPandas**
    
- Downloadable datasets and smooth filtering options
    

###  Example Charts
---

#### ➤ Renewable Energy Share Per Year
---
![https://raw.githubusercontent.com/kuranez/EU-Energy-Map/refs/heads/main/extra/images/screenshots/year_chart.png](https://raw.githubusercontent.com/kuranez/EU-Energy-Map/refs/heads/main/extra/images/screenshots/year_chart.png)

---
#### ➤ Renewable Energy Share Per Country
---
![https://raw.githubusercontent.com/kuranez/EU-Energy-Map/refs/heads/main/extra/images/screenshots/country_chart.png](https://raw.githubusercontent.com/kuranez/EU-Energy-Map/refs/heads/main/extra/images/screenshots/country_chart.png)

---
### Recent Changes
---

**Bar Charts**
- Unified display of **EU Total Average** across all charts, with a toggle option to show/hide it.
- Minor improvements to hover templates and trace labels.
	 
**Map**
- Implemented hover templates displaying **country flags and data**.
- Recentered map and adjusted zoom.
- Added layout spacers for improved alignment.

**Description**
- Added basic **usage instructions** to the dashboard.
- Added emojis and graphics.

**Layout & Dashboard**
- Reorganized dashboard components for **better clarity and user experience**.
- Minor improvements to scaling.

**File Structure**
- Reorganization of file structure to me more **modular and easier to expand**.

---

## 📦 Python Dependencies

- **Core:** `os`, `json`
    
- **Data Handling:** `pandas`, `geopandas`
    
- **Visualization:** `plotly.express`, `plotly.graph_objects`, `plotly.io`
    
- **Dashboard UI:** `panel`
    

---

## 📊 Datasets

### 1. Renewable Energy Data (Eurostat)

- **File:** `nrg_ind_ren_linear.csv`
    
- **Source:** [Eurostat – Renewable Energy](https://ec.europa.eu/eurostat/databrowser/view/nrg_ind_ren/default/table?lang=en)
    
- **Years:** 2004–2022
    
- **Columns:** Country codes, energy type, unit, value (%), flags
    
- **Categories:** Total renewables, electricity, heating/cooling, transport
    

### 2. Geographic Boundaries (GISCO - Eurostat)

- **File:** `europe.geojson`
    
- **Source:** [GISCO – Eurostat](https://ec.europa.eu/eurostat/web/gisco/geodata/administrative-units/countries)
    
- **Year:** 2024
    
- **Format:** GeoJSON (EPSG:4326), scale 1:20M
    

---

## 📁 File Structure

```yaml
EU-Energy-Map/
├── app.py                   # Main dashboard entry point
├── config.py                # Configurations (tokens, paths, etc)
├── data/
│   ├── loader.py            # Loads and merges CSV/GeoJSON data
│   ├── filters.py           # Preprocessing and filtering logic
│   └── nrg_ind_ren_linear.csv   # Eurostat renewable energy data
├── components/
│   ├── charts/
│   │   ├── bar_chart_by_country.py  # Bar chart: Country vsU
│   │   ├── bar_chart_by_year.py     # Bar chart: All countries by year
│   ├── map.py                # Interactive choropleth map
│   ├── widgets.py            # Dashboard widgets (sliders, selectors)
├── layout/
│   ├── dashboard.py          # Layout composition for Panel
├── utils/                    # Helper functions
│   ├── colors.py             # Color scales & conversion
│   ├── flags.py              # ISO2 code → emoji flag
├── assets/
│   ├── europe-renewables-500px.png  # Dashboard image
│   ├── logo-500px.png               # Logo
├── geo/
│   └── europe.geojson        # European country boundaries (GeoJSON)
```

---
## 🔗 Related Projects

If you're working with Eurostat TSV datasets and need a tool for quick conversion to CSV, check out my companion project:

➡️ **[TSV-CSV Converter](https://github.com/kuranez/TSV-CSV-Converter)** – A lightweight utility to convert Eurostat-style `.tsv` files into clean `.csv` format.

---

## 📘 License

This project is open source and available under the **MIT License**. 
You may modify, distribute, and use it freely in your own projects.

---
