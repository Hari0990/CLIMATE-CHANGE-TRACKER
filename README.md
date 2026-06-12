# 🌍 Climate Change Tracker

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-1.28-red)
![License](https://img.shields.io/github/license/Hario0990/climate-change-tracker)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen)
[![Live Demo](https://img.shields.io/badge/Live_Demo-Streamlit_Cloud-FF4B4B)](https://your-app.streamlit.app) <!-- Replace with actual demo link -->

**An interactive data visualization dashboard to track and analyze climate change indicators over time**  
[Features](#features) • [How it Works](#how-it-works) • [Architecture](#architecture) • [Data](#data) • [Installation](#installation) • [Usage](#usage) • [Demo](#demo) • [Tech Stack](#tech-stack) • [Contributing](#contributing)

---

## 📊 Overview

Climate Change Tracker is a powerful, interactive Streamlit application designed to visualize critical climate indicators including **Sea Level Rise**, **Glacier Retreat**, and **Deforestation**. The application generates animated visualizations that bring climate data to life, making it easier to understand long-term environmental trends and their implications.

![Sea level rise chart](graph_image.jpeg)  
*Average sea level change from 2000 to 2022 – an example of the animated output*

---

## ✨ Features

- 🌊 **Sea Level Rise Tracking** – Monitor average sea level changes (mm)  
- 🏔️ **Glacier Retreat Analysis** – Visualize glacier area reduction (km²)  
- 🌲 **Deforestation Monitoring** – Track forest loss (hectares)  
- 📈 **Interactive Time Series** – Dynamic animated line plots showing data evolution  
- 🎯 **Year Range Selection** – Custom slider to filter data by specific time periods  
- 📊 **Animated GIF Generation** – Automatic creation of animated visualizations for each indicator  
- 🎨 **Clean UI/UX** – Intuitive sidebar controls and streamlined interface  
- 🔄 **Real-time Data Filtering** – Instant updates based on user selections

---

## ⚙️ How It Works (Working)

The application follows a simple but effective workflow:

1. **Data Loading** – The app reads `climate_data.csv` using Pandas.  
2. **User Input** – Via the Streamlit sidebar, the user selects:  
   - Climate indicator (Sea Level Rise, Glacier Retreat, or Deforestation)  
   - Year range (e.g., 2000–2022)  
3. **Data Filtering** – The dataset is filtered to the chosen year range.  
4. **Plot Generation** – Using Matplotlib and Seaborn, a line plot is created for the selected indicator over time.  
5. **Animation** – The plot is converted into an animated GIF (using Pillow) that shows the data points appearing progressively.  
6. **Display** – The animated GIF is rendered directly in the Streamlit app.  

![Code snippet of the main app logic](code_snippet.jpeg)  
*Core logic: loading CSV, filtering, and plotting with Matplotlib*

---

## 🏗️ Architecture

The project follows a modular, data‑driven architecture:
User (Browser)
│
▼
┌──────────────────┐
│ Streamlit App │
│ (app.py) │
└────────┬─────────┘
│
▼
┌──────────────────┐ ┌──────────────────┐
│ Data Layer │────▶│ climate_data.csv │
│ (Pandas) │ └──────────────────┘
└────────┬─────────┘
│
▼
┌──────────────────┐
│ Visualization │
│ Matplotlib / │
│ Seaborn / Pillow│
└──────────────────┘

text

**Components:**

- **Frontend** – Streamlit handles all UI components (sliders, dropdowns, image display).  
- **Backend logic** – Python functions for filtering, plotting, and GIF creation.  
- **Data storage** – CSV file (easily replaceable with a database or live API).  
- **Assets** – Images, configuration files (`.streamlit/config.toml` for theming).

**Key design choices:**
- **Client‑side filtering** – Year range filtering is done in memory for speed.  
- **On‑demand GIF generation** – GIFs are created dynamically, not pre‑computed, to save storage.  
- **Modular code** – Functions like `create_animated_plot()` keep the main logic clean.

---

## 📁 Project Structure
climate-change-tracker/
├── app.py # Main Streamlit application
├── climate_data.csv # Climate dataset (required)
├── requirements.txt # Python dependencies
├── README.md # This file
├── graph_image.jpeg # Example chart image (used in README)
├── code_snippet.jpeg # Code snippet image (used in README)
├── .streamlit/
│ └── config.toml # (Optional) Custom theme
└── LICENSE # MIT License

text

---

## 📊 Data

### Data Format
Your `climate_data.csv` must contain the following columns (exact names, case‑sensitive):

| Column Name      | Data Type | Description            | Unit      |
|------------------|-----------|------------------------|-----------|
| Year             | Integer   | Year of measurement    | YYYY      |
| Sea_Level_Rise   | Float     | Sea level change       | mm        |
| Glacier_Retreat  | Float     | Glacier area loss      | km²       |
| Deforestation    | Float     | Forest area lost       | hectares  |

### Sample Data
```csv
Year,Sea_Level_Rise,Glacier_Retreat,Deforestation
2000,2.5,150.3,1200.5
2001,2.7,152.1,1250.8
2002,2.9,154.0,1300.2
2003,3.1,156.5,1350.7
2004,3.3,159.2,1400.5
Data Source
The dataset is synthetically generated for demonstration, but the structure mimics real climate data from sources like NOAA, NASA, or the IPCC. You can replace it with actual data (e.g., from Climate Data Store) as long as the column names match.

Data Quality Notes
Missing values should be handled before loading – the app assumes clean data.

All values must be numeric (floats or integers).

The Year column must have no gaps for the animation to look smooth (linear interpolation can be added if needed).

🚀 Installation
Prerequisites
Python 3.8 or higher

pip (Python package manager)

Quick Start
bash
# Clone the repository
git clone https://github.com/Hario0990/climate-change-tracker.git
cd climate-change-tracker

# Install dependencies
pip install -r requirements.txt

# Place your climate_data.csv in the root directory
# (See Data Format section above)

# Run the app
streamlit run app.py
The app will automatically open at http://localhost:8501.

📖 Usage
Select Climate Indicator – Use the sidebar dropdown to choose:

Sea Level Rise (mm)

Glacier Retreat (km²)

Deforestation (hectares)

Set Year Range – Adjust the slider to focus on a specific period (e.g., 2005–2018).

View Animation – The animated line plot will render automatically.

Download – The app generates an animated GIF that you can save (right‑click on the image in the browser).

💡 Pro Tip: Start with a broad year range to see overall trends, then narrow down for detailed analysis.

🎥 Demo
https://graph_image.jpeg
The chart above shows Sea Level Rise from 2000 to 2022. In the live app, you can switch indicators and animate through years.

Live demo: Try it on Streamlit Cloud (replace with your actual URL after deployment)

🛠️ Tech Stack
Area	Tools / Libraries
Language	Python 3.8+
Web framework	Streamlit 1.28+
Data manipulation	Pandas 2.0+
Visualization	Matplotlib 3.7+, Seaborn 0.12+
Animation/GIF	Pillow 10.0+ (Matplotlib animation API)
Theming	Streamlit config.toml + CSS
Version control	Git + GitHub
requirements.txt
txt
streamlit>=1.28.0
pandas>=2.0.0
matplotlib>=3.7.0
seaborn>=0.12.0
Pillow>=10.0.0
🎨 Customization
Theme
Create .streamlit/config.toml:

toml
[theme]
primaryColor = "#1f77b4"
backgroundColor = "#ffffff"
secondaryBackgroundColor = "#f0f2f6"
textColor = "#262730"
font = "sans serif"
Background Image
The app includes a add_bg_from_url() function – modify the URL in that function to use your own background image.

Animation Speed
In app.py, adjust the interval parameter (currently 200 milliseconds) inside the FuncAnimation call.

🤝 Contributing
Contributions are welcome! Please follow these steps:

Fork the Project

Create your Feature Branch (git checkout -b feature/AmazingFeature)

Commit your Changes (git commit -m 'Add some AmazingFeature')

Push to the Branch (git push origin feature/AmazingFeature)

Open a Pull Request

Ideas for contributions:

Add more climate indicators (temperature, CO₂ levels, Arctic ice extent)

Implement additional chart types (bar charts, heatmaps, geographic maps)

Add regional filtering (continents/countries)

Improve mobile responsiveness

Add multi‑language support (i18n)

Connect to a live API (e.g., NASA Earth Observatory)

🐛 Troubleshooting
Issue	Solution
FileNotFoundError: climate_data.csv	Ensure the CSV is in the same directory as app.py and the filename matches exactly (case‑sensitive).
KeyError: 'Year'	Check that your CSV has a column named Year (no spaces, correct case).
Animation not displaying	Verify that Matplotlib and Pillow are installed. Also ensure your data has at least two rows for an animation.
GIF looks choppy	Increase the interval value in the animation code (e.g., 300ms).
Streamlit slider showing negative values	Fix the slider range in app.py – see the code snippet in the image (the negative max was a typo).
📈 Roadmap
Basic climate indicator visualization

Animated GIF generation

Interactive year range filtering

Add temperature and CO₂ tracking

Geographic filtering (continent/country)

Export functionality (download plots as PNG/GIF)

Dashboard view with multiple indicators simultaneously

Real‑time data integration (REST API)

User authentication (optional, for saving preferences)

📜 License
Distributed under the MIT License. See LICENSE for more information.

🙏 Acknowledgments
Climate data inspiration from environmental awareness initiatives and real‑world datasets (NOAA, NASA, IPCC)

Built with ❤️ for climate action – to make scientific data accessible and engaging

Thanks to the Streamlit, Pandas, and Matplotlib communities for excellent documentation and tools

📫 Contact & Connect
Author: Hario0990 (Harithreenath Bell…)

GitHub: @Hario0990

Project Link: https://github.com/Hario0990/climate-change-tracker

If you find this project useful, please give it a ⭐ on GitHub – it helps others discover it!

