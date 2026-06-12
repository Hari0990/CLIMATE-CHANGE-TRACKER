# 🌍 Climate Data Visualizer

![Python](https://img.shields.io/badge/Python-3.9+-blue?style=flat-square&logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-1.x-red?style=flat-square&logo=streamlit)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green?style=flat-square&logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)

> An interactive climate data dashboard built with Streamlit — filter, explore, and animate historical climate trends with just a few clicks.

---

## 📌 Overview

**Climate Data Visualizer** is a data-driven web application that allows users to interactively explore climate trends across regions and time periods. Built with Python and Streamlit, it reads structured climate data, applies user-defined filters, and renders animated visualizations — making complex climate patterns easy to understand at a glance.

The dataset is synthetically generated to mimic real-world climate records (temperature, precipitation, CO₂ levels) but follows the schema of authoritative sources like **NOAA**, **NASA**, and the **IPCC**. You can swap in real data from [Copernicus Climate Data Store](https://cds.climate.copernicus.eu/) as long as the column names match.

---

## ✨ Features

| Feature | Description |
|---|---|
| 📅 Year Range Filter | Slider to select a custom time window |
| 🌐 Region Selector | Filter data by geographic region |
| 📈 Trend Plots | Line charts for temperature & precipitation trends |
| 🎞️ Animated GIFs | Auto-generated animations showing change over time |
| 📊 Statistical Summary | Mean, min, max per selected range |
| 💾 CSV Export | Download filtered data directly |
| 🎨 Seaborn Styling | Clean, publication-ready chart aesthetics |

---

## 🖼️ App Preview

### 📟 Code Snippet
![Code Snippet](code_snippet.png)

### 📊 Output Graph
![Climate Graph](graph_image.png)

---

## ⚙️ How It Works

1. **Data Loading** — `climate_data.csv` is read into a Pandas DataFrame on app startup.
2. **Filtering** — User selects year range and region via sidebar widgets; the DataFrame is sliced accordingly.
3. **Plotting** — Matplotlib + Seaborn render trend lines, bar charts, and heatmaps from the filtered data.
4. **Animation** — A GIF is generated frame-by-frame using Matplotlib's `FuncAnimation`, saved temporarily, and displayed in the Streamlit UI.
5. **Export** — Filtered data can be downloaded as a CSV with a single button click.

---

## 🏗️ Architecture

```
climate-visualizer/
│
├── app.py                  # Main Streamlit application
├── climate_data.csv        # Synthetic climate dataset
├── requirements.txt        # Python dependencies
│
├── utils/
│   ├── filters.py          # Data filtering logic
│   ├── plotter.py          # Matplotlib/Seaborn chart functions
│   └── gif_maker.py        # Animated GIF generation
│
└── README.md
```

---

## 📂 Dataset

| Column | Type | Description |
|---|---|---|
| `year` | int | Year of observation |
| `region` | str | Geographic region name |
| `temperature_c` | float | Mean annual temperature (°C) |
| `precipitation_mm` | float | Annual precipitation (mm) |
| `co2_ppm` | float | CO₂ concentration (ppm) |

- **Source:** Synthetically generated; schema mirrors NOAA/NASA datasets.
- **Real data replacement:** Download from [Climate Data Store](https://cds.climate.copernicus.eu/) and rename columns to match the schema above.

---

## 🚀 Installation

```bash
# 1. Clone the repository
git clone https://github.com/your-username/climate-visualizer.git
cd climate-visualizer

# 2. Create and activate a virtual environment
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the app
streamlit run app.py
```

---

## 🧪 Usage

1. **Select Year Range** — Use the sidebar slider to define the time window.
2. **Choose Region** — Pick one or more regions from the dropdown.
3. **Explore Charts** — View trend lines, bar charts, and heatmaps in the main panel.
4. **Watch the Animation** — Click **Generate GIF** to see an animated time-lapse of climate change.
5. **Download Data** — Click **Export CSV** to save the filtered dataset locally.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend / UI | Streamlit |
| Data Handling | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Animation | Matplotlib FuncAnimation, Pillow |
| Language | Python 3.9+ |

---

## 🌐 Live Demo

> 🔗 **[Live App →](https://your-streamlit-app-url.streamlit.app)**

---

## 📦 Requirements

```txt
streamlit
pandas
numpy
matplotlib
seaborn
pillow
```

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 👤 Author

**Hari** — AI & Robotics Developer  
[![GitHub](https://img.shields.io/badge/GitHub-your--username-black?style=flat-square&logo=github)](https://github.com/your-username)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://linkedin.com/in/your-profile)

---

<p align="center">Made with ❤️ and Python</p>
