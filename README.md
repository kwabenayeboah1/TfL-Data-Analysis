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
   git clone (https://github.com/kwabenayeboah1/TfL-Data-Analysis.git)
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

- #### Public Transport Optimisation:
Transport for London (TfL) and local authorities could leverage this data to strategically refine bus routes, introduce additional pedestrian crossings, or implement targeted speed restrictions in areas identified as accident hotspots. This proactive approach would aim to enhance commuter safety and improve the efficiency of public transport services across the network.

- #### Optimising Emergency Service Deployment
Ambulance and other emergency services could utilise predictive accident models to strategically pre-position resources in high-risk areas during peak periods. This data-driven deployment would aim to significantly reduce response times, potentially saving lives and mitigating the severity of incidents.

- #### Advancing Smart City Initiatives
Integrating this data with real-time traffic monitoring systems could facilitate dynamic adjustments to traffic light sequencing or enable congestion-based rerouting strategies. This would contribute to the development of more responsive and efficient urban environments, aligning with broader smart city objectives to optimise city functions and improve quality of life.

- #### Autonomous Vehicle Development and Validation
Developers of self-driving vehicles could utilise this comprehensive dataset to rigorously train and validate AI models. This would enable autonomous systems to more effectively identify and respond to high-risk scenarios, thereby enhancing their safety and reliability on public roads.

- #### Enhancing Cyclist & Pedestrian Safety (Vulnerable Road User Safety)
Urban planners could employ these insights to inform improvements in cycling infrastructure, establish dedicated pedestrian zones, or identify areas requiring enhanced street lighting. The objective would be to create safer environments for cyclists and pedestrians, encouraging active travel and reducing the incidence of accidents involving these vulnerable road users.

- #### Prioritising Road Infrastructure Investment
Government bodies could analyse the correlation between accident locations and prevailing road conditions, such as potholes or areas with poor visibility. This analysis would provide a robust evidence base for prioritising road maintenance and infrastructure upgrades, ensuring that investment is directed to areas where it will have the greatest impact on road safety and longevity.

## License
This project is open-source under the MIT License.

