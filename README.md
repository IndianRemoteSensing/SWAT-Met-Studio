# SWAT-Met Studio

### Daily weather data preparation for SWAT modelling

**SWAT-Met Studio** is a Windows desktop application that helps researchers and hydrological modellers download daily weather data from NASA POWER and prepare weather input files for the Soil and Water Assessment Tool (SWAT).

Define your study region, prepare a station grid, review station locations and elevations, and generate organised SWAT weather files from one workspace.

## Download and purchase

| Resource | Link |
| --- | --- |
| Software Purchase | [Official download page](https://www.indiaremotesensing.com/p/swat-met-studio-download.html) |
| Free Download from GitHub | [GitHub Releases](https://github.com/IndianRemoteSensing/SWAT-Met-Studio/releases) |
| Tutorial video | Coming soon |
| User manual | Coming soon |

<!--
When available, replace the corresponding "Coming soon" entries above with:
[Watch the tutorial](YOUR_YOUTUBE_URL)
[Read the user manual](YOUR_USER_MANUAL_URL)
-->

Download the Windows installer from the official website or GitHub Releases, install the application, and launch SWAT-Met Studio.

One trial download is available before activation. Visit the official download page for purchase and activation information.

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

Select individual variables or generate all five together.

For a workflow that includes solar radiation, **1984 or later is the recommended starting year**. The latest available dates depend on NASA POWER data availability.

### Create a station grid for your study region

- Enter the southern, northern, western, and eastern boundaries of the study area.
- Set the station spacing in decimal degrees.
- Prepare and review the adjusted grid before downloading data.
- Inspect station identifiers, coordinates, and elevations in the station table.
- Save the station table as a CSV file in a folder of your choice.

The regular grid extends the northern and eastern edges when necessary to cover the requested bounds. Station spacing controls the locations requested from NASA POWER; it does not increase the underlying weather data resolution.

### Use terrain elevations from a DEM

Choose between **NASA POWER MERRA-2 elevations** and a **user-provided Digital Elevation Model (DEM)**.

The DEM must have a valid coordinate reference system and elevations in metres.

With a DEM, you can:

- Preview the terrain with latitude, longitude, and an elevation legend.
- Use the DEM extent to define the study region.
- Display the adjusted station grid over the terrain.
- Retain stations located on valid DEM pixels.

Stations outside the DEM footprint or on NoData pixels are excluded. Elevations are sampled from the original DEM, and the source raster remains unchanged.

### Review and export station maps

Check station coverage on the terrain preview before starting a download. Export the map for reports, presentations, or research documentation.

Supported formats: **PNG, TIFF, PDF, and SVG**.

Export resolution: **72–2400 DPI**.

### Process missing weather values

The application fills missing values in downloaded records before writing the station outputs:

- Most gaps use the preceding valid value.
- Leading gaps use the first available valid value.
- Missing solar radiation values before 1984 use the average of valid solar observations returned for that station and selected period.
- Processing stops if a selected variable has no valid observations.

The processed daily records are included in the exported station CSV files. Review filled records for suitability before using them in your model.

### Generate SWAT weather inputs

Create station weather files and the corresponding station index files for the selected variables.

Index files include station identifiers, names, latitude, longitude, and elevation. Temperature files contain daily maximum and minimum temperature, in that order.

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

Completed runs use a folder name containing the selected year range and a three-digit export number, for example:

```text
SWAT_1984_2025_001/
├── SWAT_format/
├── Stations_data/
└── README.txt
```

Further exports for the same year range use the next available number, such as `002` or `003`, preserving existing results.

| Output | Purpose |
| --- | --- |
| **SWAT_format** | SWAT station weather files and station indexes |
| **Stations_data** | Daily station CSV files after missing values are filled |
| **README.txt** | Summary of the completed run |

The **SWAT_format** folder contains the selected weather outputs in one flat directory:

| Variable | Station index | Station files |
| --- | --- | --- |
| Precipitation | `pcp.txt` | `pcp1.txt`, `pcp2.txt`, … |
| Temperature | `tmp.txt` | `tmp1.txt`, `tmp2.txt`, … |
| Relative humidity | `rh.txt` | `rh1.txt`, `rh2.txt`, … |
| Solar radiation | `solar.txt` | `solar1.txt`, `solar2.txt`, … |
| Wind speed | `wind.txt` | `wind1.txt`, `wind2.txt`, … |

Each station name in an index corresponds to its weather filename. For example, `solar1` in `solar.txt` refers to `solar1.txt`.

## Who is it for?

SWAT-Met Studio supports watershed researchers, students, and hydrological modellers who need a repeatable way to prepare daily weather inputs across multiple station locations.

NASA POWER provides gridded weather data. Review the downloaded and filled records for suitability in your study area and, where possible, compare them with local observations before calibration or interpretation of model results.

## Tutorials and documentation

- **Tutorial video:** Coming soon. A YouTube link will be added here.
- **User manual:** Coming soon. A documentation link will be added here.

## Screenshots

<!--
Add software screenshots here:
- Main workspace
- DEM preview and station grid
- Station table
- Generated output folders
-->

## Developer and support

**Developer:** Lakhwinder Singh

**Email:** [swatmetstudio@gmail.com](mailto:swatmetstudio@gmail.com)

**Website:** [www.indiaremotesensing.com](https://www.indiaremotesensing.com/)

For downloads, purchase, and activation information, visit the [SWAT-Met Studio download page](https://www.indiaremotesensing.com/p/swat-met-studio-download.html).
