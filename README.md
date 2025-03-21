# TfL Incident Analysis (2005-2006)

## Overview:
This is an analysis of Data provided using the Transport for London API for incidents reported on the network between the years 2005-2006.
The analysis focuses on visualizing accident locations using an interactive map and clustering techniques to identify high-risk areas.
It also highlights the severity of accidents and the vehicles involved to give greater insight into the type of accidents occuring within London, how frequent they are and the vehicles involved.

## Analysis Approach:
1. **Data Source**: The dataset consists of incident reports from TfL for 2005 and 2006. While additional years are available, this project initially focuses on these two years as a means of understanding how the data was initially collated.
2. **Visualization**: Incident locations are plotted on an interactive map using the Folium package.
3. **Clustering**: Accidents are grouped to identify high-density accident zones. This also maens it is less intensive on the system the script is being ran on and allows for easier viewing.
4. **Findings**:
   - Certain locations exhibited consistently high incident rates, which may indicate hazardous road conditions or high traffic density.
   - Where incidents have been logged twice with differing IDs, assumption that TfL has logged the incident in accordance with the number of individuals involved (e.g - an accident with 3 vehicles would be logged thrice with differing IDs)

## Technologies Used:
- **Postman**: Used to download the response.json once TfL is accessed via the API Key
- **Folium**: For interactive map visualization.
- **JSON Parsing**: Extracting data from the TfL API response by parsing the JSON into the attritubes required.
- **Jupyter Notebook**: Used for executing the analysis. Ease of use and readability makes Jupyter great for this kind of analysis.

## How to Run the Project:
### Prerequisites
1. **Sign up for a TfL API Key**: The dataset is obtained via an API request (https://api.tfl.gov.uk/).
2. **Download the relevant JSON via Postman**: The data for 2005/2006 has already been provided, however for further analysis, use of the Postman Client will allow you to download subsequent years.
3. **Download the JSON response**: Once authenticated, download the dataset and save it as `response.json` with the subsequent year.
4. **Install Dependencies**:
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
3. Place your `response.json` file in the same directory.
4. Open the Jupyter Notebook and execute the script to generate the interactive map. Once all dependencies are installed, run the script. A HTML Map will be produced and saved in your working directory, as well as a map that can be accessed via the Jupyter Notebook console.

## Future Improvements
- Expand analysis to include additional years.
- Possibility to combine and compare years in a single Map interface
- Possibility to introduce Machine Learning to highlight areas prone to accidents and predict where areas in the future may require due attention
- Incorporate severity analysis across the years to determine the trend in severity as London learns to commit to safer roads

## Contributing
Contributions are welcome! Feel free to fork this repository, make improvements, and submit a pull request. I am always looking to learn, if there are any improvements to the code please feel free.

## License
This project is open-source under the MIT License.

## Assumptions about the Data
- Assume that accidents are recorded in tandem with the number of people involved. I have inferred this because there are entries that are identical in attributes with differing IDs. I have not had contact with TfL to determine whether this is the case, but would be beneficial to know just so analysis on the data is accurate.

## Possible Use-Cases
I imagine that such data could be enriched with other data (weather data, rush hour data) to make it more viable for use. I envision Insurance companies would be very interested in understanding how such data could be used to calculate premiums and moniter insruance costs for those in high/low risk areas.
I also believe it is something the Government could potentially leverage in making our roads safer for use by introduced or updating road signage in London to prevent a high number of accidents. 

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



