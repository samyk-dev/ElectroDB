# ElectroDB  - Electrode Process Optimization Suite

ElectroDB is a comprehensive Streamlit application for battery researchers to calculate electrode slurry recipes, manage electrode databases, and analyze coating uniformity.

## 📑 Table of Contents

- [About the Project](#about-the-project)
- [Support & Contact](#-support--contact)
- [Quick Start](#-quick-start-guide)
- [Features](#features)
- [User Guide](#-user-guide)
- [Database Management](#database-management)
- [Pro Tips](#pro-tips)
- [Troubleshooting](#-troubleshooting)
- [Workflow Integration Suggestions](#workflow-integration-suggestions)
- [Acknowledgements & Usage](#acknowledgments--usage)
- [Connect & Learn More](#connect--learn-more)

---

## About the Project

ElectroDB is an ongoing free, open-source project maintained by Samy Kouidri, an undergraduate at the University of Chicago studying Molecular Chemical Engineering. As a scientist passionate about streamlining electrochemical research workflows, I apply mathematical rigor, scientific principles, and systematic problem-solving to develop structured tools that improve research processes and accelerate battery development.

## 📞 Support & Contact

Have questions, suggestions, or found a bug?
I'm dedicated to improving ElectroDB and welcome your feedback!

Email: skouidri@uchicago.edu
Please include "ElectroDB" in the subject line for priority response

I'll do my best to:

- Answer technical questions
- Implement reasonable feature requests
- Fix reported bugs promptly
- Provide guidance on advanced usage

---

## 📋 Quick Start Guide

### 🌐 Web Version
Ready to dive right in?
Access the live web application instantly:

[Access the Project Here](https://electrodb.streamlit.app/)

Click above to start using ElectroDB immediately in your browser!

### 💻 Local Installation
Prefer to run ElectroDB locally? Follow these steps:

**Prerequisites:**
- Python 3.7+
- pip (Python package manager)

**Installation:**
1. **Clone or download the ElectroDB.py code** to your local machine
2. **Install required dependencies:**
   ```bash
   pip install streamlit pandas numpy matplotlib seaborn plotly scipy xlsxwriter fpdf openpyxl
   ```
3. **Run the application:**
   ```bash
   streamlit run ElectroDB.py
   ```
4. **Open your browser** to the local URL shown in the terminal (typically `http://localhost:8501`)

---
## Features

### 1. Slurry Calculator
- Multi-component formulation tracking
- Dilution history management
- Mass balance calculations
- Export recipes to Excel

### 2. Blade Height Recommender
- Linear regression analysis
- Confidence intervals
- Historical data integration
- Database-aware recommendations

### 3. Capacity Match Tool
- Cathode/anode capacity balancing
- Areal capacity calculations
- Automatic blade height estimation

### 4. Coating Calibration
- Grid-based uniformity analysis
- Multiple visualization modes (Deviation, Critical, Spec)
- 3D plate representation
- Statistical uniformity scoring

### 5. Database Manager
- Form-based data entry
- Filtering and searching
- Import/export functionality
- Statistical overviews

---

## 📋 User Guide

### First Time Setup
1. **Create a database file**: In the sidebar, make sure the database file path is correct (default: `electrode_database.xlsx`)
2. **Click "Create empty DB if missing"** to initialize your database

### Using the Slurry Calculator
1. **Select "Slurry Calculator"** from the sidebar
2. **Set your formula ratios**: Active Material %, Conductive Carbon %, Binder %
3. **Choose your target**: Either specify active mass or total slurry mass
4. **Configure components**: Expand sections to specify multiple active materials, carbons, binders, or solvents
5. **View your recipe**: The app automatically calculates all component masses
6. **Track dilutions**: Use the dilution tracker to manage solvent additions

### Adding Electrodes to Database
1. **Select "Electrode Database Manager"** from the sidebar
2. **Go to the "Add Electrodes" tab**
3. **Fill in the form**:
   - Electrode type (Cathode/Anode)
   - Active material (choose from library or custom)
   - Substrate details
   - Processing parameters
   - Binder and conductive additive information
4. **Click "Add to Database"** - mass loadings are automatically calculated!

### Estimating Blade Height
1. **Select "Blade Height Recommender"** from the sidebar
2. **Choose data source**: Use your database or built-in historical data
3. **Select material and filters**
4. **Set target mass loading**
5. **View the regression analysis** and recommended blade height

### Capacity Matching
1. **Select "Capacity Match Tool"** from the sidebar
2. **Enter known electrode details** (material, mass loading, capacity)
3. **Set capacity ratio** (N/P or P/N)
4. **Enter target electrode properties**
5. **View required mass loading** and blade height recommendation

### Coating Calibration
1. **Select "Coating Calibration Tool"** from the sidebar
2. **Set up your coating matrix** (rows × columns)
3. **Enter measured masses** for each position
4. **View heatmaps and 3D visualizations** of coating uniformity
5. **Export calibration reports**

---

## Database Management

### Supported Columns
Your electrode database includes:
- **Basic Info**: Electrode Type, Active Material, Substrate, Diameter
- **Masses**: Total mass, Tare weight, Mass Loading, Active ML
- **Processing**: Solid %, Blade Height, Active Material %
- **Composition**: Binder Type, Binder %, Conductive Material, Conductive %
- **Metadata**: Date Made, Made By, Notes

### Import/Export
- **Import**: Excel files with matching column structure
- **Export**: Download as Excel or CSV for analysis
- **Missing values**: Mass Loading and Active ML are auto-calculated on import

---

## Pro Tips

1. **Start with the database**: Add a few electrodes first to build your historical data
2. **Use consistent naming**: For materials and substrates to enable better filtering
3. **Export regularly**: Backup your database using the export feature
4. **Leverage historical data**: The more electrodes you add, the better the blade height recommendations become
5. **Use the coating tool**: For quality control and process optimization

---

## ❗ Troubleshooting

###  Common Issues

1. **"Permission denied" error**:
   - Try a different filename in the sidebar
   - Make sure the file isn't open in Excel
   - Make sure the imported file is in .xlsx format
   - Run as administrator if needed

2. **Missing mass loading values**:
   - Ensure all required columns are filled when importing
   - The app will auto-calculate missing values when importing a database

3. **Visualization issues**:
   - Make sure all required packages are installed
   - Check browser console for errors

### 🆘 Getting Help
If you encounter issues:
1. Check that all dependencies are installed
2. Ensure your Excel files have the correct column structure
3. Verify file permissions for database read/write
4. If these fixes do not work, contact skouidri@uchicago.edu with "ElectroDB" in the subject line to get help, I will try to respond as soon as possible

---

## Workflow Integration Suggestions

1. **Planning a new formulation?** → Use the Slurry Calculator to speed up calculations
2. **Coating electrodes?** → Use the Blade Height Recommender to achieve specific mass loading targets
3. **Measuring results?** → Add mass measurements to Database to build a future reference
4. **Analyzing uniformity?** → Use the Coating Calibration Tool to visualize any potential defects or trends
5. **Optimizing the manufacturing process?** → Record parameters in Database Manager to build knowledge over time
6. **Balancing electrodes for new coin cells?** → Use the Capacity Match Tool

---

## Acknowledgments & Usage

### Feedback and Support

If you find ElectroDB useful in your research, I would greatly appreciate:

   - Feedback and suggestions for improvements

   - Mention or reference if you use it in publications or presentations

   - Credit if you build upon or adapt this work for similar projects

### Special Thanks

I would like to extend my sincere gratitude to:

   - [Dr. Mitchell Kaiser](https://www.cei.washington.edu/people/mitchell-kaiser/) (Postdoctoral Scholar) for his invaluable guidance and mentorship throughout this project

   - The University of Washington [Energy Materials Research Group](https://sites.uw.edu/junliuuwgroup/) (Prof. Jun Liu's group) for their input, testing, and help in refining the project

   - All beta testers who provided feedback during development

This tool was developed to serve the battery research community, and I hope it helps labs optimize their electrode workflows so researchers can focus on what matters most: building better batteries and advancing the bigger picture of energy storage solutions.

---

## Connect & Learn More

Access my Professional Background and Resume:
[Download Samy Kouidri's Resume](https://docs.google.com/presentation/d/1_B3E1VeladcI55Si75HNcuhIB7MdSo0Gfo2sL5IAdNk/export?format=pdf)

Let's connect on Linkedin:
[🔗 Samy Kouidri on LinkedIn](https://www.linkedin.com/in/samy-kouidri-55a799302/)
