# Fixed Broadband Coverage Analysis (2019 - 2023)

# Project Background
This project analyzes broadband coverage across the United Kingdom from 2019 to 2023, focusing on key metrics such as Superfast Broadband (SFBB), Ultrafast Broadband (UFBB), Full Fibre, and Gigabit availability. The primary goals is to evaluate broadband accessibility, identify trends, and uncover disparities across local authority areas. Data from Ofcom's broadband report was utilised, ensuring the findings are grounded in reliable sources.

# Data Structure & Initial Checks

The dataset was derived from Ofcom's annual reports and structured to span 374 local authorities over five years, resulting in 1870 records. Key steps in data preparation included: 

* **Initial Inspection:** Ensured data completeness and absence of duplicates.
* **Cleaning:** Addressed inconsistencies across CSV files, such as varying column names and ambiguous data.
* **Storage:** Data was structured and stored in a MongoDB database for accessibility and further analysis. Columns included broadband availability metrics, local authority names and codes.
* **Summary:** The dataset was analysed using Pandas to verify integrity, showing clean and usable records with proper alignment across years.

# Executive Summary

### Overview of Findings

#### Overall Trends

* Broadband availability across the UK has improved significantly between 2019 and 2023.
* SFBB coverage grew from 93.62% in 2019 to 96.07% in 2023.
* Full Fibre availability experienced a sharp increase, rising from 8.59% to 47.6%.
* Gigabit broadband availability showed the most dramatic growth, increasing from 8.5% to nearly 70%.
* Premises below USO declined substantially, reflecting improvements in access to basic broadband speeds.

#### Regional Insights

* Urban areas generally have higher broadband speeds and availability.
* Rural areas, especially the Orkney and Shetland Islands, show significant gaps in coverage.

# Insights Deep Dive
### Regional Trends

* **Aberdeen City:** Full Fibre availability surged by 6.5 times, growing from 16,410 premises in 2019 to 107,315 in 2023. Corresponding decreases were observed in premises below the Universal Service Obligation (USO) threshold, dropping nearly 5 times (189 in 2019 to 40 in 2023). This growth indicates robust infrastructure investment and a targeted effort to expand access to high-speed internet.

<div align="center">
    <img src="./aberdeen_city_full_fibre_vs_below_uso.jpg" alt="Description of Image" width="85%">
</div>

* **York:** In contrast to Aberdeen, York showed modest growth in broadband infrastructure. Full Fibre availability increased by just 1.47 times (from 43,077 premises in 2019 to 63,736 in 2023). Interestingly, York experienced a reduction in matched premises, with 1,966 fewer properties between 2019 and 2023. This may be due to urban redevelopment or shifting population dynamics.

* **Orkney and Shetland Islands:** These island regions lag significantly, with 16.7% and 16% of premises, respectively, unable to receive 10Mbit/s broadband speeds as of 2023.
Geographical challenges such as their remote locations and higher infrastructure costs likely contribute to this disparity.

<div align="center">
    <img src="./top_10_areas_below_USO.png" alt="Description of Image" width="85%">
</div>

### Broadband Type Analysis

* **Superfast Broadband (SFBB):** Nearly universal, increasing from 93.62% in 2019 to 96.07% in 2023. This modest growth reflects a mature infrastructure and focuses on improving connectivity quality rather than expanding the network. Despite high coverage, rural areas still report inconsistencies in meeting the 30Mbit/s threshold.

* **Ultrafast Broadband (UFBB):** Availability grew from 47% in 2019 to 70% in 2023, with the most significant annual increase (8.4%) observed between 2021 and 2022. The disparity between urban and rural areas is stark, as rural localities often struggle with cost-effective deployment.

* **Ultrafast Broadband (100 Mbit/s+):** One of the fastest-growing segments, jumping from an estimated 49% (inferred) in 2019 to 71.81% in 2023. Steady annual growth of approximately 5.6% indicates ongoing infrastructure upgrades, with large-scale investments aligning with government initiatives for digital inclusion.

* **Gigabit Broadband:** Showed exponential growth, from 8.5% in 2019 to 70% in 2023—a 62% increase over five years. Significant increases in 2021 and 2022 (26.37% in one year) underscore the pandemic-driven urgency to upgrade networks to meet surging demand for remote work and education.

* **Full Fibre Availability:** A parallel growth to Gigabit broadband was observed, with availability increasing from 8.59% in 2019 to 47.6% in 2023. Full Fibre's increasing importance is evident in its role as the backbone for Gigabit-capable networks.

<div align="center">
    <img src=".//trends_in_broadband_coverage_over_period.png" alt="Description of Image" width="85%">
</div>


### Coverage Gaps

* **Premises Below USO:** The percentage of premises unable to receive broadband speeds below 2Mbit/s, 5Mbit/s, and 10Mbit/s has steadily declined over the years. Premises below the 10Mbit/s threshold decreased from 2.1% in 2019 to 1.24% in 2023, highlighting ongoing progress but leaving notable gaps in underserved regions.

<div align="center">
    <img src="./trends_in_premises_unable_to_receive_low_broadband_speeds.png" alt="Description of Image" width="70%">
</div>

* **Islands and Remote Regions:** Island regions such as Orkney and Shetland face persistent challenges, with logistical and financial barriers to deploying high-speed broadband. These areas also report limited Full Fibre and Gigabit availability, reflecting infrastructure disparities.

### Observational Patterns

* **Pandemic-Driven Trends:** The sharpest increases in high-speed broadband availability (e.g., Full Fibre and Gigabit) occurred between 2020 and 2022, during the COVID-19 pandemic.
Factors contributing to this surge include remote work and education demands; reduced road traffic, facilitating quicker infrastructure deployments.

* **Urban vs Rural Divide:** Urban areas consistently exhibit higher broadband availability due to cost-efficient infrastructure deployment. Rural areas, particularly in Scotland and Wales, lag significantly, underlining the need for targeted investments.

* **Policy Impacts:** Initiatives such as the Universal Service Obligation (USO), launched in 2020, correlate with increased focus on underserved areas. Legislation and funding have accelerated improvements, particularly in regions previously unable to meet basic speed thresholds.

### Reccomendations

* **Infrastructure Investments:** Prioritize underserved regions, particularly rural and island communities, to reduce digital inequality. Expand Full Fibre and Gigabit coverage to align with urban availability levels.

* **Policy Initiatives:** Incentivize broadband providers to target remote areas. Implement subsidies or public-private partnerships for high-cost infrastructure projects.

* **Monitoring and Reporting:** Establish regular updates to track progress and assess policy effectiveness. Enhance data granularity to understand local challenges better.

### Assumptions and Caveats

* **Data Completeness:** Assumes the dataset fully represents the broadband availability landscape across the UK.

* **Urban vs. Rural Bias:** The analysis highlights that urban areas often show higher coverage due to cost-efficient infrastructure deployment.
  
* **Limitations of Percentage Metrics:** While percentages normalize data for comparison, they may mask absolute disparities in larger or denser regions.
