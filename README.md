# Colorado Snowfall Analysis and XCast Toolkit Integration

## Overview

This repository includes the Colorado Snowfall Analysis Project, which explores historical snowfall and temperature trends across key Colorado cities, and provides instructions for installing and utilizing the XCast toolkit for advanced climate forecasting.

### What is XCast?
XCast is a free and open-source climate forecasting toolkit developed by Kyle Hall & Nachiketa Acharya. It empowers forecasters and earth scientists to apply state-of-the-art postprocessing techniques to gridded datasets. Learn more on the [XCast documentation site](https://xcast-lib.github.io/).

## Colorado Snowfall Analysis

### Data Cleaning

Each dataset was cleaned for uniformity and accuracy:
- Replaced missing or erroneous values (e.g., `-998`, `-999`) with `NaN`.
- Standardized column names (e.g., `SNWD` to `snowcover`).
- Created unified `date` columns.
- Then drop any remaining NaN values.

### Key Analyses

1. **Snowfall Trends**: Seasonal and daily snowfall trends were visualized with cumulative summaries.
2. **Temperature Analysis**: Analyzed daily, monthly, and seasonal temperatures using regression models.
3. **Monthly Averages**: Insights into average snowcover and temperature changes by month.

### Visualizations

All plots are saved under `plots/` in subfolders for each city:
- Daily and cumulative snowfall trends.
- Temperature trends with regression analysis.
- Seasonal and monthly summaries.

---

## Installation

### Installing XCast

XCast is available on Anaconda and can be installed with the following command:

```bash
conda install -c conda-forge -c hallkjc01 xcast
```

To set up an environment with Jupyter Notebook for XCast, use:

```bash
conda create -n xcast_env -c conda-forge -c hallkjc01 xcast xarray netcdf4 jupyter ipykernel 
conda activate xcast_env 
python -m ipykernel install --name=xcast_env --user 
```

You can then select `xcast_env` as the kernel in Jupyter Notebook.

> **Note**: XCast installation might require you to manually downgrade certain packages. If you encounter any issues, please refer to the [XCast documentation](https://xcast-lib.github.io/).

### Running Snowfall Analysis

1. Clone the repository.
2. Ensure cleaned weather data files are in the `data/` folder.
3. Use the Python notebooks to run city-specific analyses
4. Visualizations will be generated in `plots/`.

---

## License

Distributed under the MIT License. See `LICENSE` for more information.

---

## Contact

- For issues with the Colorado Snowfall Analysis project: Please make an issue in this repository.
- For XCast-specific queries: [Open an issue here](https://github.com/kjhall01/xcast/issues).

---

## Acknowledgements

- Weather data sourced from [NOAA](https://www.noaa.gov/).
- XCast toolkit by Kyle Hall & Nachiketa Acharya.