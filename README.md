# 🌍 Climate Change Tracker

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-1.0+-red.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Maintenance](https://img.shields.io/badge/Maintained-Yes-brightgreen.svg)
![Data Visualization](https://img.shields.io/badge/Data-Visualization-orange.svg)

**An interactive data visualization dashboard to track and analyze climate change indicators over time**

[Features](#-features) • [Demo](#-demo) • [Installation](#-installation) • [Usage](#-usage) • [Data Format](#-data-format) • [Technologies](#-technologies) • [Contributing](#-contributing)

</div>

---

## 📊 Overview

Climate Change Tracker is a powerful, interactive Streamlit application designed to visualize critical climate indicators including **Sea Level Rise**, **Glacier Retreat**, and **Deforestation**. The application generates animated visualizations that bring climate data to life, making it easier to understand long-term environmental trends and their implications.

## ✨ Features

- 🌊 **Sea Level Rise Tracking** - Monitor average sea level changes measured in millimeters
- 🏔️ **Glacier Retreat Analysis** - Visualize glacier area reduction measured in square kilometers
- 🌲 **Deforestation Monitoring** - Track forest loss measured in hectares
- 📈 **Interactive Time Series** - Dynamic animated line plots showing data evolution over time
- 🎯 **Year Range Selection** - Custom slider to filter data by specific time periods
- 📊 **Animated GIF Generation** - Automatic creation of animated visualizations for each indicator
- 🎨 **Clean UI/UX** - Intuitive sidebar controls and streamlined interface
- 🔄 **Real-time Data Filtering** - Instant updates based on user selections

## 🎥 Demo

> **Note:** Add an animated GIF demo here showcasing your app in action.

## 🚀 Installation

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Quick Start

1. **Clone the repository**
git clone https://github.com/yourusername/climate-change-tracker.git
cd climate-change-tracker

text

2. **Install required dependencies**
pip install -r requirements.txt

text

3. **Prepare your data**

Ensure you have a `climate_data.csv` file in the root directory. See [Data Format](#-data-format) section below.

4. **Run the application**
streamlit run app.py

text

5. **Open your browser**

The app will automatically open at `http://localhost:8501`

## 📖 Usage

### Basic Workflow

1. **Select Climate Indicator**: Use the sidebar dropdown to choose from:
- Sea Level Rise (mm)
- Glacier Retreat (km²)
- Deforestation (hectares)

2. **Set Year Range**: Adjust the slider to select your desired time period

3. **View Animation**: Watch the animated visualization render automatically

4. **Download**: The app generates and displays animated GIFs for each indicator

## 📊 Data Format

Your `climate_data.csv` file should contain the following columns:

| Column Name | Data Type | Description | Unit |
|------------|-----------|-------------|------|
| `Year` | Integer | Year of measurement | YYYY |
| `Sea_Level_Rise` | Float | Sea level change | mm |
| `Glacier_Retreat` | Float | Glacier area loss | km² |
| `Deforestation` | Float | Forest area lost | hectares |

### Sample Data

Year,Sea_Level_Rise,Glacier_Retreat,Deforestation
2000,2.5,150.3,1200.5
2001,2.7,152.1,1250.8
2002,2.9,154.0,1300.2
2003,3.1,156.5,1350.7
2004,3.3,159.2,1400.5

text

## 📁 Project Structure

climate-change-tracker/
│
├── app.py # Main Streamlit application
├── climate_data.csv # Climate dataset (required)
├── requirements.txt # Python dependencies
├── README.md # Project documentation
└── LICENSE # License file

text

## 🛠️ Technologies

- **[Python](https://www.python.org/)** - Core programming language
- **[Streamlit](https://streamlit.io/)** - Web application framework
- **[Pandas](https://pandas.pydata.org/)** - Data manipulation and analysis
- **[Matplotlib](https://matplotlib.org/)** - Static plotting library
- **[Seaborn](https://seaborn.pydata.org/)** - Statistical data visualization
- **[Pillow](https://pillow.readthedocs.io/)** - GIF generation and image processing

## 📦 Requirements

Create a `requirements.txt` file with:

streamlit>=1.28.0
pandas>=2.0.0
matplotlib>=3.7.0
seaborn>=0.12.0
Pillow>=10.0.0

text

## 🎨 Customization

### Custom Styling

Create a `.streamlit/config.toml` file in your project:

[theme]
primaryColor = "#1f77b4"
backgroundColor = "#ffffff"
secondaryBackgroundColor = "#f0f2f6"
textColor = "#262730"
font = "sans serif"

text

### Adding Background Image

The app includes a custom background feature. Modify the `add_bg_from_url()` function in `app.py` to add your preferred background image URL.

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Contribution Ideas

- 🌟 Add more climate indicators (temperature, CO2 levels)
- 📊 Implement additional visualization types
- 🗺️ Add geographic/regional data filtering
- 📱 Improve mobile responsiveness
- 🌐 Multi-language support
- 📈 Statistical analysis features

## 🐛 Troubleshooting

### Common Issues

**CSV file not found error:**
- Ensure `climate_data.csv` is in the same directory as `app.py`
- Check the file name spelling and case sensitivity

**Year column missing error:**
- Verify your CSV has a column named exactly `Year`
- Ensure there are no extra spaces in column names

**Animation not displaying:**
- Check that your data has sufficient rows for animation
- Verify matplotlib and Pillow are properly installed

## 📈 Roadmap

- [x] Basic climate indicator visualization
- [x] Animated GIF generation
- [x] Interactive year range filtering
- [ ] Add temperature and CO2 tracking
- [ ] Implement geographic filtering
- [ ] Export functionality for visualizations
- [ ] Dashboard view with multiple indicators
- [ ] Real-time data integration

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🌟 Acknowledgments

- Climate data visualization inspired by environmental awareness initiatives
- Built with ❤️ for climate action
- Thanks to the Streamlit community for excellent documentation

## 💡 Tips for Users

- **Best Practices**: Start with a broad year range to see overall trends, then narrow down for detailed analysis
- **Data Quality**: Ensure your CSV file has no missing values for accurate visualizations
- **Performance**: Large datasets may take longer to animate; consider filtering to smaller year ranges
- **Customization**: Modify the animation speed by adjusting the `interval` parameter in the code (currently set to 200ms)

---

<div align="center">

**⭐ Star this repository if you found it helpful!**

Made with ❤️ and ☕

![Visitors](https://visitor-badge.laobi.icu/badge?page_id=yourusername.climate-change-tracker)

</div>
