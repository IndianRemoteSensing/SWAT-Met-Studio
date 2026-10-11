# SWAT-Met Studio

### Daily weather data preparation for SWAT modelling

**SWAT-Met Studio** is a Windows desktop application that helps researchers and hydrological modellers download daily weather data from NASA POWER and prepare weather input files for the Soil and Water Assessment Tool (SWAT).

Define your study region, prepare a station grid, review station locations and elevations, and generate organised SWAT weather files from one workspace.

## What you can do

### Download daily weather data

Choose a year range and download the weather variables needed for your study:

| Weather variable | Daily information |
| --- | --- |
| Precipitation | Daily precipitation |
| Temperature | Maximum and minimum temperature |
| Relative humidity | Daily relative humidity |
| Solar radiation | Daily solar radiation |
| Wind speed | Daily wind speed |

Select individual variables or generate all five together. For a workflow that includes solar radiation, use 1984 or later as the starting year. The latest available dates depend on NASA POWER data availability.

### Create a station grid for your study region

- Enter the southern, northern, western, and eastern boundaries of the study area.
- Set the station spacing in decimal degrees.
- Prepare and review the adjusted grid before downloading data.
- Inspect station identifiers, coordinates, and elevations in the station table.

The regular grid extends the northern and eastern edges when necessary to cover the requested bounds. Station spacing controls the locations requested from NASA POWER; it does not increase the underlying weather data resolution.

### Use terrain elevations from a DEM

Use NASA POWER MERRA-2 elevations or select a Digital Elevation Model (DEM) with a valid coordinate reference system and elevations in metres.

With a DEM, you can use its extent to define the study region and retain stations located on valid terrain pixels. Stations outside the DEM footprint or on NoData pixels are excluded. Elevations are sampled from the original DEM, and the source raster remains unchanged.

### Review and export station maps

View the station grid on a map alongside the terrain preview. Check the spatial coverage before starting a download, then export the map for reports, presentations, or research documentation.

Supported map formats: **PNG, TIFF, PDF, and SVG**, with export resolution from **72 to 2400 DPI**.

### Prepare continuous daily records

The software processes downloaded records and fills missing values before writing station outputs. You can inspect the processed daily records in the exported station CSV files.

### Generate SWAT weather inputs

Create station weather files and the corresponding station index files for the selected variables. Index files include station identifiers, names, latitude, longitude, and elevation. Temperature files contain daily maximum and minimum temperature in that order.

Each completed export is saved in a separate run folder, keeping earlier results available.

## A simple workflow

1. **Define the region** — enter geographic bounds, a year range, and station spacing.
2. **Choose elevations** — use NASA POWER elevations or select a DEM.
3. **Prepare the grid** — review the station table and map.
4. **Select weather variables** — choose the data needed for your SWAT project.
5. **Choose an output folder and generate** — download, process, and export the weather records.
6. **Review the results** — inspect the summary and station data before using the files in SWAT.

An internet connection is required to download NASA POWER weather data.

## What is included in an export?

A completed run contains:

| Output | Purpose |
| --- | --- |
| **SWAT_format** | SWAT station weather files and station indexes |
| **Stations_data** | Daily station CSV files after missing values are filled |
| **README.txt** | Summary of the completed run |

The **SWAT_format** folder contains the selected weather outputs in one flat directory:

| Variable | Station index | Station files |
| --- | --- | --- |
| Precipitation | pcp.txt | pcp1.txt, pcp2.txt, … |
| Temperature | tmp.txt | tmp1.txt, tmp2.txt, … |
| Relative humidity | rh.txt | rh1.txt, rh2.txt, … |
| Solar radiation | solar.txt | solar1.txt, solar2.txt, … |
| Wind speed | wind.txt | wind1.txt, wind2.txt, … |

## Who is it for?

SWAT-Met Studio supports watershed researchers, students, and hydrological modellers who need a repeatable way to prepare daily weather inputs across multiple station locations.

NASA POWER provides gridded weather data. Review the downloaded and filled records for suitability in your study area and, where possible, compare them with local observations before calibration or interpretation of model results.

## Screenshots

<!-- Add software screenshots here: main workspace, DEM and station map, station table, and generated output. -->

## Support

For software enquiries, contact [swatmetstudio@gmail.com](mailto:swatmetstudio@gmail.com).
