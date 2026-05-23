# NASA Exoplanet Data Analysis

## Project Overview

This project analyzes real exoplanet data from NASA's Exoplanet Archive using Python and Jupyter Notebook.

The goal of this project is to explore relationships between planetary size, temperature, host stars, and potentially habitable planets through data visualization and exploratory data analysis.

## Tools Used

- pandas
- numpy
- matplotlib
- seaborn
- plotly
- kaleido
- jupyterlab

## Dataset Informaion

Data was obtained from NASA's Exoplanet Archive:

https://exoplanetarchive.ipac.caltech.edu/

The dataset was retrieved using NASA's Exoplanet Archive API and includes information about confirmed exoplanets such as:

- Planet radius
- Planet mass
- Equilibrium temperature
- Host star temperature
- Distance from Earth

## Project Structure

```text
nasa-exoplanet-analysis/
├── data/
├── notebooks/
├── images/
├── docs/
│   └── interactive_exoplanet.html
├── README.md
└── requirements.txt
```

## Project Goals

This analysis explores scientific questions, such as:

- Are larger planets generally hotter?
- Which planets may exist in the habitable zone?
- How do host star temperatures affect planets?
- What trends exist among confirmed exoplanets?

## Dataset Features and Scientific Units

| Feature | Description | Unit |
|---|---|---|
| `pl_bmasse` | Planet mass | Earth masses |
| `pl_rade` | Planet radius | Earth radii |
| `pl_eqt` | Planet equilibrium temperature | Kelvin (K) |
| `st_teff` | Host star effective temperature | Kelvin (K) |
| `sy_dist` | Distance from Earth to planetary system | Parsecs |

### Earth-Relative Measurements

Many planetary measurements are expressed using Earth-relative units, allowing easier comparison between discovered exoplanets and Earth.

For example:

- A planet mass value of `1` represents a planet with the same mass as Earth.
- A planet radius value of `1` represents a planet with the same radius as Earth.
- Values greater than `1` indicate planets larger or more massive than Earth.
- Values smaller than `1` indicate planets smaller or less massive than Earth.

Earth itself is not included in the dataset; instead, Earth is used as the reference baseline for comparison.


## Data Visualizations

### Distribution of Exoplanet Sizes

![Planet Radius Distribution](images/radius_distribution.png)

### Planet Size vs Temperature

![Temperature vs Radius](images/planet_temperature.png)

### Potentially Habitable Planets

![Potentially Habitable Planets](images/habitable_exoplanets.png)

### Interactive Exoplanet Explorer

![Static Preview of Exoplanet Explorer](images/interactive_exoplanet.png)

>Click to open interactive version: [Open Interactive Exoplanet Explorer](https://morganm4951-debug.github.io/nasa-exoplanet-analysis/interactive_exoplanet.html)

### Feature Correlations

![Habitable Planets](images/feature_correlations.png)


## Key Interpretations

- Large-radius planets within the dataset are interpreted to most likely be gas giant exoplanets because planets with radii significantly larger than Earth typically contain gaseous atmospheres.
- Planets with radii smaller than approximately 2 Earth radii are interpreted to most likely be rocky planets  since smaller-radius planets are more likely to possess solid terrestrial surfaces.
- Candidate habitable planets were identified using temperatures between 200 K and 320 K and radii smaller than 2 Earth radii. 

## Key Findings
- Several exoplanets fall within approximate habitable-zone temperature ranges based on their equilibrium, temperature, and planetary radius. 
- Most confirmed exoplanets in the dataset are significantly larger than Earth, with gas giant planets representing a substantial amount of those detected discoveries. 
- Extremely hot exoplanets appear frequently throughout the dataset, indicating that many of the planets that we can detect currently orbit very close to their stars.
- Smaller rocky planets occur less frequently in the dataset, indicating that many of them we may be unable to currently detect.
- Analysis of planetary equilibrium temperature and planetary radius indicate that planets orbiting hotter stars or existing at closer orbital distances generally had higher overall temperatures.
- Larger exoplanets exhibited a wider range of masses and equilibrium temperatures compared to smaller rocky planets, suggesting greater detectable physical diversity among planetary systems that are likely to be gas giant planetary systems.

## Project Limitations

- Although several planets fall within approximate habitable-zone thresholds, equilibrium temperature alone cannot determine true planetary habitability. Factors such as atmospheric composition, magnetic fields, surface pressure, water availability, orbital stability, and stellar radiation exposure are not included in this analysis.

- Planet equilibrium temperature values are theoretical estimates rather than direct measurements of planetary surface conditions.

- Current exoplanet catalogs are affected by observational bias because existing detection methods more easily identify large planets orbiting close to their host stars. Smaller rocky planets may therefore be underrepresented within the dataset.

- Some planetary records contain missing or incomplete measurements, reducing the usable sample size for certain visualizations and correlation analyses. The dataset was also limited to the first 5,000 records retrieved from the NASA Exoplanet Archive and as such does not represent the complete catalog of confirmed exoplanets.

- Correlation analysis identifies statistical relationships between variables but does not establish direct causal relationships between planetary or stellar characteristics.

## How to Run This Project Locally

1. Clone the repository:
   git clone https://github.com/morganm4951-debug/nasa-exoplanet-analysis.git

2. Enter the project folder:
   cd nasa-exoplanet-analysis

3. Create a Virtual Environment:
   Windows:
        python -m venv venv
        venv\Scripts\activate

    Mac/Linux:
        python -m venv venv
        source venv/bin/activate

4. Install dependencies:
   pip install -r requirements.txt

5. Start JupyterLab:
   jupyter lab

6. Open the notebook:
   notebooks/exoplanet_analysis.ipynb

7. Run all cells:
   Kernel → Restart Kernel and Run All
