# Sales Win-Rate Diagnostics and Revenue Forecast Engine - SkyGeni Assessment

1. Approach:
   This project is developed as part of coding assessment for Data Science / Applied AI Engineer role.
   The task is to invesigate a business problem where the sales win rates are declining over recent quarters despite a healthy pipeline volume. The solution follows a structured, data-driven approach combining Exploratory analysis, diagnostics metrics, forecasting logic and a alert system design.
   The workflow is organised into four layers:
   - Step 1: Exploratory Data Analysis (EDA)
     This section contains deal-level data analysis across industry, region, product_type, lead_source, deal_size and time. The goal is to identify where the win-rate decline is originating.
     
   - Step 2: Diagnostic Metrics
     In addition to overall win-rate, diagnostic metrics were also generated such as:
      - Segment win-rate comparison
      - Pipeline Quality indicators
      - Stage conversion behaviour
      - Probability weighted expected revenue
      
   - Step 3: Rule based Revenue Forecast Engine
     A rule-based prbability models was built using historic win data by different attributes(industry, lead_source, deal_size_band). Active deals are assigned an estimate win probability and coverted to expected revenue forecast.

   - Step 4: Insight & Alert System Design
     A lightweight alert framework designed to monitor:
     - segment performance drop
     - pipeline risk concentration
     - stage aging issue
     - lead source quality decline

     These rule-driven alerts can be extended to have a predefined recommended action mapping that can also suggest recommeneded action to mitigate the alert.

2. How to run this project
   Prerequisites
    - Python 3.9+
    - pandas
    - numpy
    - matplotlib

   Install dependencies:
     pip install pandas, numpy, matplotlib

    Input Data:
     Provide the CSV file in the same directory as this notebook. In case working with google colab, upload the required CSV file.

    Execution:
     Run the notebook using local environment or Google colab
     
3. Key Decisons
   - Rule based model instead of a ML based model
     A simple rule based model was implemented to ensure interpretability, low implementation risk and alignment with the assignment constraints.
   - Probability-weighted Forecasting
     The forecasting system uses probability-weighted revenue rather than pipeline totals to avoid overestimation and give realistic results.
   - Median Metrics over Averages
     Median sales cycle and median deal-size were preferred over averages to reduce distortion from outliers
   - Batch Scheduling instead of Real-Time
     The insight and alert system is designed for daily and weekly batches as it is sufficient for sales decision cycles and will keep the infrastructure lightweight

4. Summary
   This project deliver a practical, interpretable sales diagnostics and forecasting framework that identifies where the win-rate decline originates, estimates realistic revenue and produce alerts. 
   
