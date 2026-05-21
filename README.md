# NASA Exoplanet Data Analysis

## Project Overview

This project analyzes real exoplanet data from NASA's Exoplanet Archive using Python and Jupyter Notebook.

The goal of this project is to explore relationships between planetary size, temperature, host stars, and potentially habitable planets through data visualization and exploratory data analysis.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- Jupyter Notebook

## Dataset Source

Data was obtained from NASA's Exoplanet Archive:

https://exoplanetarchive.ipac.caltech.edu/

The dataset was retrieved using NASA's Exoplanet Archive API and includes information about confirmed exoplanets such as:

- Planet radius
- Planet mass
- Equilibrium temperature
- Host star temperature
- Distance from Earth

## Project Goals

This analysis explores several scientific questions:

- Are larger planets generally hotter?
- Which planets may exist in the habitable zone?
- How do host star temperatures affect planets?
- What trends exist among confirmed exoplanets?

plt.savefig("../images/temp_vs_radius.png")

## Example Visualizations

### Planet Radius Distribution

![Planet Radius Distribution](images/radius_distribution.png)

### Planet Temperature vs Radius

![Temperature vs Radius](images/temp_vs_radius.png)

### Potentially Habitable Planets

![Habitable Planets](images/habitable_planets.png)

## Key Findings

- Most confirmed exoplanets are larger than Earth.
- Extremely hot planets are common in current discoveries.
- Smaller rocky planets appear less frequently in the dataset.
- Several planets fall within approximate habitable-zone temperature ranges.
- Host star temperature appears related to planetary equilibrium temperature.

## Project Structure

nasa-exoplanet-analysis/

- ├──data/
- ├── notebooks/
- ├── images/
- ├── README.md
- └── requirements.txt

## Example Visualizations

### Planet Radius Distribution

![Planet Radius Distribution](images/radius_distribution.png)

## How to Run

1. Clone the repository

```bash
git clone https://github.com/morganm4951-debug/nasa-exoplanet-analysis.git

2. Install dependencies

pip install -r requirements.txt

3. Launch Jupyter Notebook
jupyter notebook

4. Open:
notebooks/exoplanet_analysis.ipynb
