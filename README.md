# UPI - Dashboard

### Dashboard Link :  https://app.powerbi.com/groups/me/dashboards/c1b1c071-9b1b-4ad6-922b-c3c03e4a7ea3?experience=power-bi
 
## Problem Statement
 
 With the rapid growth of digital payments in India, UPI (Unified Payments Interface) has emerged as a dominant mode of transaction. However, stakeholders often lack a clear understanding of how UPI transactions vary across time, location, demographic groups, and platforms.
 
This project aims to address the following key problems:

What are the monthly trends in UPI transaction volumes and values throughout the year 2024?

Which apps, banks, and cities contribute most to UPI usage?

How do user demographics (age, gender) and device types impact transaction behavior?

Are there any seasonal patterns or spikes/dips in digital payment activity?

How can this data be interactively explored by stakeholders for insights and decision-making?

By visualizing this data in Power BI, we enable a deeper understanding of digital payment adoption and performance in different segments, aiding banks, fintech companies, and policymakers.



### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a Excel file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present.
- Step 5 :   A custom column "AgeGroup" was added using DAX to classify customers into three age brackets:

A1: Age ≤ 25

A2: Age 26–35

A3: Age > 35

This helps in visualizing UPI transaction trends across different age demographics and understanding user behavior patterns by generation.

  Age Group = IF(Sheet1[CustomerAge] <= 25, "A1",
           IF(Sheet1[CustomerAge] <= 35, "A2", "A3"))

- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 : Since the data contains various ratings, thus in order to represent ratings, a new visual was added using the three ellipses in the visualizations pane in report view. 
- Step 8 : Visual filters (Slicers) were added for eight field named "Bankname sent", "bankname recieve", "Purpose" , "device"
,"City" , "Gender" , "PaymentMethod" , "TrasactionType" , "AgeGroup" & "MerchantName".

  ![Slicers FR](https://github.com/Puneet1223/UPI-Dashboard2/blob/167ce23d6eb1b1e3c00d00dfea81436b02331592/slicersfr.png?raw=true)


- Step 9 :  Select the line chart to  displays the monthly trend of UPI transactions throughout the year 2024. It helps visualize how transaction volumes fluctuate over time, highlighting key peaks and drops.
             
  ![Line Chart for Amount](https://github.com/Puneet1223/UPI-Dashboard2/blob/0281c324295244f5b1087016910607fdf72e52ff/line%20chart%20for%20amount.png?raw=true)

   
- Step 10 : Add a column chart over the line chart to visualizes the total UPI transaction amounts for each month in 2024.
It provides a clear and comparative view of the monthly flow of digital payments.

The tallest bar in May indicates the highest transaction value, showing peak usage.

A dip in August reflects a temporary drop in transaction activity.

This chart complements the line chart by offering a strong visual comparison of month-to-month changes in total UPI payment values.
 
     
 ![Column Chart for Amount](https://github.com/Puneet1223/UPI-Dashboard2/blob/37be462615bdcc920a150916d54885300b24def0/Column%20chart%20for%20amount.png?raw=true)



- Step 11 :  Select another line chart over the two chart in same page This line chart displays the remaining UPI account balance at the end of each month.
It provides a visual trend of how the user's or system’s available balance fluctuates over time.

Helpful for tracking spending vs saving behavior.

Highlights months with low or high retained balances.

This chart is useful for identifying financial peaks, declines, and potential savings patterns over the year.
 
  ![Line Chart for Balance](https://github.com/Puneet1223/UPI-Dashboard2/blob/e5feb2f57fc33781daf1372ec6d0f0ec51b88358/line%20chart%20for%20balance%20.png?raw=true)


- Step 12 : Another column chart added in the same page over all three charts this column chart offers a bar-based comparison of the monthly remaining balances.
Each bar represents the total balance left after all UPI transactions for that month.

Allows easier side-by-side comparison between months.

Useful for detecting sudden dips or gains in balance retention.

 ![Column Chart for Balance](https://github.com/Puneet1223/UPI-Dashboard2/blob/0c5818a1ead7bd73d20c56958e81f127eb6ed014/column%20chart%20for%20balance.png?raw=true)



- Step 13 :  Now To enhance the user experience, the dashboard uses Power BI Bookmarks, the Selection Pane, and Navigator Buttons to allow users to switch between multiple charts on the same page. This avoids clutter and keeps the visual focus clean.

Key features:

📌 Only one chart is visible at a time, based on user selection.

🔘 Navigation buttons are provided to toggle between views (e.g., Line Chart, Column Chart, Pie Chart, etc.).

🏷️ Charts are layered in the Selection Pane, and Bookmarks are used to capture each chart’s visibility state.

How it works:

Charts are stacked one above the other.

Each button triggers a Bookmark that shows only the selected chart.

Seamless transitions provide an app-like interactive experience.

Benefits:

Cleaner and more focused visuals.

Users can explore data one insight at a time.

Mimics a multi-page experience without switching tabs.

   ![Betns Image](https://github.com/Puneet1223/UPI-Dashboard2/blob/c3f054f0c8e60d0e15036d47975488ff3c3f0f77/betns.png?raw=true)


- Step 14 :   To complement the visual analysis from Page 1, this page presents the same UPI transaction data in a tabular format for precise, granular insights.
- Step 15 :  The table breaks down monthly UPI transaction data for major cities: Bangalore, Delhi, Hyderabad, and Mumbai.

Columns include:

Month

Currency

Amount

Remaining Balance

       
 - Step 16 :  Each city’s data is displayed in its respective currency unit (EUR, USD, GBP, INR).

     ![Table View](https://github.com/Puneet1223/UPI-Dashboard2/blob/f339fe7638efc2b7dd7980c8105bc19be0563cce/Table_View.png?raw=true)

 
 - Step 17 : Conditional formatting is applied to highlight significant values in "Amount" and "Remaining Balance" columns (in pink), helping quickly identify highs and lows.
 
 - Step 18 :  The page retains all the slicers from Page 1 to allow dynamic filtering by:

Bank, City, Device, Gender

Purpose, Age Group, Transaction Type, etc.

This layout allows users who prefer detailed data tables over visuals to review and analyze transaction behavior with precision. It is especially useful for:

Data auditors

Financial analysts

Compliance reviewers

 - Step 19 : All necessary visuals, filters, and interactivity features have been implemented.

The report ensures both insightful analytics and detailed data access.

It is now ready to be shared with stakeholders via Power BI Service or exported as needed.

This concludes the dashboard development process.
