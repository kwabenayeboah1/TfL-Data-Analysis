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
   git clone [https://github.com/kwabenayeboah1/TfL-Data-Analysis.git]
   ```
2. Navigate to the project directory:
   ```sh
   cd TfL-Data-Analysis
   ```
3. Place your `response.json` file(s) in the same directory.
4. Open the Jupyter Notebook and execute the script to generate the interactive map. Once all dependencies are installed, run the script. A HTML Map will be produced and saved in your working directory, as well as a map that can be accessed via the Jupyter Notebook console. The script dynamically names the generated map based on the year suffix found in the .json file. 


### Statistics
Once the .ipynb file is executed with the relevant JSON input, the Jupyter Notebook will render an interactive Incident Map. Furthermore, the execution will populate the console output with a series of calculated statistics, providing a quantitative summary of the data. The subsequent section outlines the specific statistical outputs you can expect to see. 

These stats were derived from the 2006 .json dataset.

### Key Metrics Overview
<img width="1841" height="1361" alt="image" src="https://github.com/user-attachments/assets/fb691811-f6a4-4cbc-a093-b469bc70130b" />

* Drawing from the 2006 dataset, this analysis delivers key statistics that offer a comprehensive understanding of incident distribution across London's boroughs. Crucially, the output will identify the incident categories with the highest frequency, clearly indicating the specific borough where each peak occurred and the corresponding total number of incidents. 

### Analysis of Categories of Severity per Borough
<img width="2037" height="867" alt="image" src="https://github.com/user-attachments/assets/d0ab9625-d59a-4c60-821d-fecd602a0336" />

* Beyond identifying high-incident areas, the notebook will further dissect the data to present a categorical breakdown of incidents. Crucially, for each incident category, it will pinpoint the London borough demonstrating the lowest recorded number of occurrences (as well as the highest recorded number), thereby offering valuable comparative insights into areas of relative safety or successful mitigation. When this analysis is repeated across the datasets spanning the years 2005-2019, it would effectively highlight trends in successful mitigation strategies or identify areas becoming increasingly prone to incidents.

### Analysis of Vehicle Type and Incident Involvement
<img width="822" height="854" alt="image" src="https://github.com/user-attachments/assets/629e79f4-70df-41a1-83b5-7cfc29f60a4b" />

* A detailed understanding of the vehicle types involved in such incidents is paramount for developing and implementing appropriate safety features and policies throughout London, thereby contributing to overall road safety improvements. Furthermore, comprehending the proportional representation of various vehicle types in accident statistics would be highly beneficial for discerning comparative safety trends and formulating effective incident mitigation plans

### Analysis of Casualties per Vehicle Type
<img width="1299" height="839" alt="image" src="https://github.com/user-attachments/assets/aab85605-c82e-44af-a32b-f160b9e4d1a1" />

* Our analysis provides a view of casualties occurring across the transport network. It is important to note that the dataset does not explicitly distinguish between minor injuries, serious injuries, and fatalities. Therefore, for the purpose of this analysis, the assumption has been made that 'casualties' refers to any individual who would have sought medical treatment as a direct result of an incident.
* To enhance the granularity and utility of this dataset, a future improvement could involve extracting incidents with known fatalities and comparing these figures against the overall number of casualties. This would allow for a more nuanced understanding of incident severity and the nature of this dataset that has been provided by TfL.
* Regardless of this distinction, the current data remains highly insightful, providing crucial information on the number of individuals affected by incidents. This understanding is invaluable for informing strategies to further improve road safety. Furthermore, if access to more detailed information regarding the technology and design of various transport modes were available, this casualty data could be leveraged to drive advancements in vehicle safety features and infrastructure design.

### Severity of Incidents per Vehicle Type
<img width="1491" height="893" alt="image" src="https://github.com/user-attachments/assets/ebde9b80-51f3-4229-8517-dca4b32b910f" />

* The data on vehicle types involved in incidents offers a critical lens through which to assess road safety. By understanding this composition with the severity of incidents, we can identify specific areas for intervention, such as the implementation of bespoke safety features across London. This insight is also invaluable for tracking comparative safety trends over time and for developing targeted strategies to mitigate future incidents.


### Breakdown of Fatal Incidents by Vehicle Type
<img width="825" height="662" alt="image" src="https://github.com/user-attachments/assets/2b671caf-3855-49dd-a420-a5e99e88e2e2" />

* To address the most severe consequences of incidents, a focused analysis on fatal occurrences, broken down by vehicle type, is indispensable. The gravity of these events, which result in the loss of life, underscores the necessity of understanding their precise nature. By identifying patterns in their locations and characteristics, we can generate actionable intelligence to inform targeted interventions and significantly enhance efforts to prevent such incidents from recurring.
* Our analysis includes a comprehensive view of casualties that have occurred on the transport network. It is important to clarify the definition of 'casualty' within this dataset. Based on the available information, and consistent with common practice in road safety reporting in the UK, the data does not explicitly differentiate between minor, serious, and fatal injuries within a single 'casualty' count.
* Therefore, for the purpose of this analysis, we operate under the assumption that a 'casualty' refers to any individual who sustained an injury in an incident and would have sought, or required, medical attention as a direct result. Fatalities, which represent the loss of life, are typically recorded as a distinct category due to their severe nature and specific reporting requirements. This distinction explains why the total number of 'casualties' and 'fatalities' may not directly sum, as a fatality is a specific type of outcome rather than just an injury requiring medical help.
* To further enhance the analytical depth of this dataset, a valuable future step would be to explicitly extract and analyse incidents that resulted in known fatalities. This would allow for a direct comparison with the overall casualty figures, providing a more granular understanding of incident severity and its most tragic outcomes.
* Regardless of this definitional nuance, the current data remains profoundly insightful. It provides critical information on the total number of people who have been adversely affected by incidents, offering a robust foundation for informing strategies to improve road safety. Furthermore, this data could be instrumental in driving advancements in the technology and design of various transport modes, particularly if more detailed information regarding vehicle specifications and infrastructure design were to become accessible


### Breakdown of Peak Times for Fatal Incidents
<img width="866" height="1034" alt="image" src="https://github.com/user-attachments/assets/d54f8228-ae48-4a60-a7bf-a018141db5bc" />

* Our analysis further delves into the temporal distribution of fatal incidents, specifically identifying the hours of the day when these tragic events are most prevalent. This breakdown, ordered from the most common hour of occurrence to the least, provides crucial insights into the peak risk periods on the transport network.
* By pinpointing these high-risk hours, stakeholders such as emergency services, transport authorities, and road safety organisations can strategically allocate resources, enhance surveillance, and implement targeted preventative measures. For instance, increased police presence, focused road safety campaigns, or dynamic traffic management strategies could be deployed during these identified peak times to mitigate the likelihood of fatal incidents.
* Understanding these hourly patterns also contributes to a more comprehensive risk assessment, allowing for the development of time-sensitive interventions aimed at reducing the most severe outcomes on London's roads. This granular temporal insight is invaluable for optimising safety efforts and working towards a safer transport environment.


### Breakdown of Peak Months for Fatal Incidents
<img width="836" height="590" alt="image" src="https://github.com/user-attachments/assets/311e61aa-84c5-4cc6-9248-adfd6061bc04" />

* This output identifies the number of incidents recorded per Month. The most common month with the highest number of incidents is highlighted at the top of the output. This analysis provides a critical temporal overview, highlighting periods when the network experiences its greatest incidence of the most severe outcomes. Understanding these peak months is fundamental for targeted risk management and preventative action.

Identifying the months with the highest fatal incidents is an exceptionally useful and critical metric for road safety analysis, offering immediate and actionable insights for strategic interventions.

This metric directly points to periods of elevated risk, which is crucial for:
* Targeted Resource Allocation: Knowing which months consistently experience more fatalities allows authorities (e.g., TfL, emergency services, police) to strategically deploy additional resources, increase surveillance, or enhance enforcement during these high-risk periods.
* Informing Safety Campaigns: This data can guide the timing and messaging of public awareness campaigns. For instance, if a particular month shows a spike in pedestrian fatalities, a campaign focusing on pedestrian safety could be launched in the preceding weeks.
* Identifying Correlating Factors: High incident months often correlate with other significant factors such as:
   * Seasonal Conditions: Adverse weather (e.g., rain, ice, fog), reduced daylight hours, or specific road conditions prevalent in certain months.
   * Increased Traffic Volume: Holiday periods, school terms, or specific events that lead to higher vehicle and pedestrian movements.
   * Behavioural Changes: Changes in driver or pedestrian behaviour linked to seasonal activities or events.
* Driving Policy and Infrastructure Review: Consistent peaks in certain months can prompt a review of existing policies, speed limits, or infrastructure design specific to those periods or the conditions prevalent within them.
* Benchmarking and Trend Analysis: Tracking these high-risk months over time allows for the assessment of whether interventions are effective in reducing fatalities during these periods, or if new patterns of risk are emerging.

However, while highly valuable, it's important to contextualise this metric with further analysis to understand the underlying reasons for these peaks. For example, a high number of incidents in December might be due to a combination of increased traffic, darker evenings, and potentially adverse weather, rather than just the month itself. Therefore, this metric is most powerful when analysed in conjunction with:

* Traffic Volume Data: To determine if higher incidents are simply a function of more exposure.
* Weather Data: To assess the impact of environmental conditions.
* Incident Type and Vehicle Category Data: To understand what kind of fatal incidents are peaking.
* Operational Changes: Any specific interventions or changes in transport operations during those months.

In conclusion, the 'months with the highest fatal incidents' is a foundational and highly actionable metric. It provides clear direction for where and when to focus safety efforts, and its utility is maximised when integrated with other relevant datasets to uncover the root causes of these elevated risks, thereby informing robust, evidence-based preventative strategies.


### Breakdown of Peak Months for Fatal Incidents
<img width="1011" height="735" alt="image" src="https://github.com/user-attachments/assets/cd0f0902-4404-4283-b29b-ab8fbecd690c" />

* A detailed examination of incident frequency on a monthly basis would be highly insightful for identifying recurring patterns and trends across the calendar year. It is plausible that a direct link exists between certain months and incident rates, especially when accounting for external variables such as seasonal changes. For instance, the prevalence of snow or ice during winter months could significantly increase the likelihood of incidents. Understanding these seasonal correlations could inform predictive models and targeted preventative measures

### Breakdown of Fatalities per Borough
<img width="720" height="1287" alt="image" src="https://github.com/user-attachments/assets/a8b5bbbe-8f95-4afa-83ad-7f46cedb1152" />

* A crucial aspect of our analysis involves examining the distribution of fatal incidents across London's boroughs. This breakdown, presented in descending order from the borough with the highest number of fatalities to the lowest, provides a stark geographical overview of the most severe outcomes on the transport network.
* By identifying the boroughs that experience a disproportionately higher number of road fatalities, this analysis serves as a vital tool for prioritising resources and intervention strategies. It allows stakeholders, such as TfL and local councils, to focus their efforts on specific areas where the risk to life is greatest. This granular understanding can inform targeted road safety campaigns, infrastructure improvements, and policy adjustments designed to mitigate the occurrence of fatal incidents in these high-risk locations.
* Conversely, boroughs with consistently lower fatality rates may offer valuable insights into successful road safety practices or urban planning strategies that could be replicated elsewhere. This comparative analysis is essential for working towards the Vision Zero goal of eliminating all road deaths and serious injuries

### Breakdown of Incidents per Weekday
<img width="806" height="408" alt="image" src="https://github.com/user-attachments/assets/3e0be93a-e433-48a8-b813-280c1adc3ea8" />

* The analysis includes a statistical breakdown identifying the number of incidents per weekday. It highlights which days typically experience a greater number of incidents, offering a basic temporal understanding of when incidents are more likely to happen.

* While identifying the most common day for an incident provides a foundational temporal insight, its standalone utility as a metric for deep analytical insights or targeted intervention is somewhat limited.
* On its own, knowing that, for example, 'Thursday' is the most common day for incidents doesn't immediately explain why this is the case. It's a descriptive statistic that points to a pattern but lacks explanatory power. The underlying causes are likely multifaceted and influenced by other factors that correlate with specific days, such as:
• Traffic Volume: Weekdays, particularly rush hours, naturally have higher traffic volumes, increasing exposure to risk.
• Commuting Patterns: The start and end of the working week often see different types of journeys and driver behaviours.
• Social Activities: Weekends, or specific evenings, might correlate with increased leisure travel, different vehicle mixes, or factors like impaired driving.
• Operational Hours: Public transport operations and commercial vehicle movements vary by day.

* Therefore, while it serves as a useful starting point for temporal analysis, its true value emerges when cross-referenced with other variables. For instance, combining the 'most common day' with 'peak hours', 'incident categories', 'vehicle types involved', or 'causality factors' would yield far more actionable intelligence. For example, if Fridays consistently show a higher number of pedestrian incidents during evening hours, this points to a more specific problem that can be addressed with targeted interventions.

* In summary, the 'most common day for an incident' is a foundational descriptive statistic. It's a good initial indicator but requires further contextualisation and integration with other data points to become a truly powerful and actionable metric for informing road safety strategies.

### Incomplete Data Consolidation
<img width="825" height="1269" alt="image" src="https://github.com/user-attachments/assets/06942221-fc90-4bbe-9e65-90832f8f6263" />

* This output provides a clear and concise overview of incidents where key metrics were not fully recorded within the JSON dataset. For each identified incident, the output will specify which particular data fields are absent or incomplete. This systematic identification of missing data points is crucial for understanding the overall completeness and reliability of the dataset.

* Identifying and detailing incidents with incomplete data records is an absolutely essential metric for any robust data analysis and governance framework. Its utility is multifaceted and profoundly impacts the integrity and potential of the entire dataset:
• Data Quality Assessment: This output serves as a primary indicator of data quality. It quantifies the extent of missing information, allowing for an objective assessment of the dataset's completeness and potential biases.
• Informing Data Enrichment Strategies: By pinpointing precisely which metrics are frequently missing, this analysis directly informs strategies for data enrichment. For example, if 'contributing_factor' is consistently absent, it highlights a specific area where supplementary data collection or integration from other sources (e.g., police reports, witness statements) could significantly enhance the dataset's analytical power.
• Understanding Data Collection Processes: Frequent gaps in specific fields can indicate issues within the data collection process itself. This insight can be invaluable for improving data capture mechanisms, training personnel, or refining reporting protocols to ensure more comprehensive data in the future.
• Mitigating Analytical Bias: Awareness of missing data allows analysts to account for potential biases in their findings. If certain types of incidents are more prone to incomplete records, this knowledge can prevent erroneous conclusions.
• Guiding Future Data Integration: If external datasets are being considered for integration, understanding the existing gaps helps in identifying which external sources would provide the most valuable supplementary information.

* In essence, this output moves beyond merely acknowledging data limitations; it provides the granular detail necessary to strategically address them. It transforms a known weakness into an actionable roadmap for data improvement, ultimately enhancing the reliability and depth of any subsequent analysis. Therefore, this is not just a useful metric, but a foundational one for data integrity and future analytical development



## Future Improvements
- **Expanded Temporal Analysis** Expand analysis to include additional years. [Completed Jan 2026]
-  **Multi-Year Map Interface** Implement the capability to combine and compare data from multiple years within a single interactive map interface. [Completed - Glob Package can be used to combine years within the CD]
- **Predictive Modelling** Introduce Machine Learning techniques to identify accident-prone areas and forecast future locations requiring attention.
- **Severity Trend Analysis** Incorporate a cross-year severity analysis to ascertain trends in accident severity, reflecting London's commitment to safer roads.
- **Environmental Factors** Investigate the potential influence of weather data and statistics on accident occurrences, where feasible.
- **Further Dataset Addition** Understand whether supplementary data could improve the data we have, as well as fill in any missing gaps within the current datasets. One such example would be police reports to further enrich some of the incidents recorded.

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

