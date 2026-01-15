# TfL Incident Analysis

## Overview:
This repository analyses Transport for London (TfL) Incident Data from the years 2005-2019, sourced via the OpenAPI protocol provided by TfL. It features interactive visualisations of accident locations, employing clustering algorithms to identify areas with high-risk. Incidents recorded feature accident severity and the types of vehicles involved, providing granular insights into incident characteristics and prevalence within London Boroughs.

## Analysis Approach:
1. **Data Source**: The datasets have been sourced from TfL's OpenAPI Protocol, which features recorded incidents from the years 2005-2019. An additional script to determine the number of .jsons downloadable is also included, to determine if/when TfL add further datasets from 2019 onwards.
2. **Visualisation**: Incident locations are plotted on an interactive map using the Folium package.
3. **Clustering**: Accidents are grouped to pinpoint high-density accident zones. This approach also reduces system resource intensity and facilitates easier viewing. If the script is used to combine more than one dataset, this will prove beneficial considering the high number of incidents.
4. **Findings & Limitations**:
   - Certain locations consistently exhibited high incident rates, potentially indicating hazardous road conditions or significant traffic density.
   - Where incidents have been logged twice with differing IDs, the assumption is that TfL has recorded the incident according to the number of individuals involved (e.g., an accident with three vehicles would be logged thrice with distinct IDs).


## Technologies + Notable Packages Used:
- **Folium**: Utilised for interactive map visualisation.
- **JSON Parsing**: Employed for extracting necessary attributes from the TfL API's JSON responses.
- **Jupyter Notebook**: The primary environment for executing the analysis, chosen for its ease of use and readability in data exploration.

## How to Run the Project:
### Prerequisites

1. **Install Dependencies**:
   ```sh
   pip install -r requirements.txt
   ```
### Running the Analysis
1. Clone this repository:
   ```sh
   git clone [https://github.com/your-username/TfL-Data-Analysis.git](https://github.com/kwabenayeboah1/TfL-Data-Analysis.git](https://github.com/kwabenayeboah1/TfL-Data-Analysis.git)
   ```
2. Navigate to the project directory:
   ```sh
   cd TfL-Data-Analysis
   ```
3. Place your `response.json` file(s) in the same directory.
4. Open the Jupyter Notebook and execute the script to generate the interactive map. Once all dependencies are installed, run the script. A HTML Map will be produced and saved in your working directory, as well as a map that can be accessed via the Jupyter Notebook console. The script dynamically names the generated map based on the year suffix found in the .json file. 

## Future Improvements
- **Expanded Temporal Analysis** Expand analysis to include additional years. [Completed Jan 2026]
-  **Multi-Year Map Interface** Implement the capability to combine and compare data from multiple years within a single interactive map interface. [Completed - Glob Package can be used to combine years within the CD]
- **Predictive Modelling** Introduce Machine Learning techniques to identify accident-prone areas and forecast future locations requiring attention.
- **Severity Trend Analysis** Incorporate a cross-year severity analysis to ascertain trends in accident severity, reflecting London's commitment to safer roads.
- **Environmental Factors** Investigate the potential influence of weather data and statistics on accident occurrences, where feasible.

## Contributing
Contributions are welcome! Feel free to fork this repository, make improvements, and submit a pull request. I am always looking to learn, if there are any improvements to the code please feel free.

## Assumptions about the Data
**Incident Recording Methodology**
- It is assumed that incidents are recorded in tandem with the number of individuals involved. This inference is drawn from observations of entries with identical attributes but differing IDs. Direct confirmation from Transport for London (TfL) would be beneficial to ensure the accuracy of subsequent data analysis.


## Possible Use-Cases
This data, particularly when enriched with supplementary information such as weather patterns or rush hour statistics, holds significant potential for various applications. 

**Insurance Sector**
- Insurance providers could leverage this analysis to refine premium calculations and monitor insurance costs more effectively, differentiating between high and low-risk areas.

**Government & Road Safety**
Governmental bodies could utilise these insights to enhance road safety initiatives in London. This might involve introducing new road signage or updating existing infrastructure in accident-prone areas to mitigate incident frequency.

- #### Public Transport Planning:
TfL and local councils could use this data to adjust bus routes, add pedestrian crossings, or implement speed restrictions in accident-prone areas.
- #### Emergency Response Optimization
Ambulance and emergency services could use predictive accident models to pre-position vehicles in high-risk areas during peak times, reducing response time.
- #### Smart City Initiatives
Integration with real-time traffic monitoring could allow for dynamic traffic light adjustments or congestion-based rerouting.
- #### Autonomous Vehicle Training
Self-driving car companies could use this data to train AI models to identify high-risk areas and adjust driving behavior accordingly.
- #### Cyclist & Pedestrian Safety
City planners could use this to improve cycling infrastructure, create pedestrian zones, or identify areas needing better lighting.
- #### Road Maintenance & Infrastructure Upgrades
The government could analyze the correlation between accident locations and road conditions (e.g., potholes, poor visibility) to prioritize repairs.

## License
This project is open-source under the MIT License.

