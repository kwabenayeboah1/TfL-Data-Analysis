# TfL Incident Analysis (2005-2006)

## Overview
This is an analysis of Data provided using the Transport for London API for incidents reported on the network between the years 2005-2006.
The analysis focuses on visualizing accident locations using an interactive map and clustering techniques to identify high-risk areas. It also highlights the severity of accidents and the vehicles involved to give greater insight into the type of accidents occuring within London and how frequent they are.

## Analysis Approach
1. **Data Source**: The dataset consists of incident reports from TfL for 2005 and 2006. While additional years are available, this project initially focuses on these two years.
2. **Visualization**: Incident locations are plotted on an interactive map using Folium.
3. **Clustering**: Accidents are grouped to identify high-density accident zones.
4. **Findings**:
   - Year-on-year accidents increased, though severity levels varied.
   - Certain locations exhibited consistently high incident rates, which may indicate hazardous road conditions or high traffic density.

## Technologies Used
- **Folium**: For interactive map visualization.
- **JSON Parsing**: Extracting data from the TfL API response.
- **Jupyter Notebook**: Used for executing the analysis.

## How to Run the Project
### Prerequisites
1. **Sign up for a TfL API Key**: The dataset is obtained via an API request.
2. **Download the JSON response**: Once authenticated, download the dataset and save it as `response.json`.
3. **Install Dependencies**:
   ```sh
   pip requirements.txt
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
4. Open the Jupyter Notebook and execute the script to generate the interactive map.

## Future Improvements
- Expand analysis to include additional years.
- Incorporate severity analysis.
- Use machine learning models to predict accident-prone areas.

## Contributing
Contributions are welcome! Feel free to fork this repository, make improvements, and submit a pull request.

## License
This project is open-source under the MIT License.

---

Let me know if you need any modifications or additional sections! 🚀

