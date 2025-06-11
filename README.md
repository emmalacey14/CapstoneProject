## Google Analytics Final Capstone
### By Emma Lacey

[My Google Analytics Certificate](#)  
[My Tableau Dashboard](#)

### Data Analysis Process

The case study follows the six-step data analysis process:



<ul class="icon-list">
<li data-icon="❓">

<strong>[Ask](#Ask) </strong>

</li>
<li data-icon="💻">

<strong>[Prepare](#prepare)</strong>

</li>
<li data-icon="🛠">

<strong>[Process](#process)</strong>

</li>
<li data-icon="📊">

<strong>[Analyse](#analyse)</strong>

</li>
<li data-icon="📋">

<strong>[Share](#share)</strong>

</li>
<li data-icon="🧗‍♀️">

<strong>[Act](#act)</strong>

</li>
</ul>

### Scenario

Since its launch in 2013, Bellabeat has evolved from a promising
start-up into a recognised leader in women’s wellness technology. As the
company sets its sights on global expansion, it is leveraging the power
of user data to unlock new strategic opportunities.

------------------------------------------------------------------------

#### Project Goal

-   **Analyse** smart device usage data from a key Bellabeat product to
    uncover how users engage with its wellness technology.  
-   **Translate** those insights into targeted, data-driven marketing
    recommendations that directly support strategic decision-making and
    business growth.  
-   **Demonstrate** the impact of data analytics in shaping the future
    of a forward-thinking, wellness-focused brand.

------------------------------------------------------------------------

### Step 1. Ask

------------------------------------------------------------------------

#### 1.1 Business Task:

**Analyse FitBit Fitness Tracker Data** to gain insights into how
consumers are using the FitBit app and discover trends and insights for
**Bellabeat marketing strategy**.

------------------------------------------------------------------------

#### 1.2 Business Objectives:

1.  What are the trends identified?  
2.  How could these trends apply to Bellabeat customers?  
3.  How could these trends help influence Bellabeat marketing strategy?

------------------------------------------------------------------------

#### 1.3 Deliverables:

1.  A clear summary of the business task  
2.  A description of all data sources used  
3.  Documentation of any cleaning or manipulation of data  
4.  A summary of analysis  
5.  Supporting visualizations and key findings  
6.  High-level content recommendations based on the analysis

------------------------------------------------------------------------

#### 1.4 Key Stakeholders:

1.  **Urška Sršen**: Bellabeat’s cofounder and Chief Creative Officer  
2.  **Sando Mur**: Mathematician, Bellabeat’s cofounder and key member
    of the Bellabeat executive team  
3.  **Bellabeat marketing analytics team**: A team of data analysts
    guiding Bellabeat’s marketing strategy.

------------------------------------------------------------------------

### Step 2. Prepare

------------------------------------------------------------------------

#### 2.1 Data Source Overview

The dataset used for this analysis is publicly available on Kaggle:  
[FitBit Fitness Tracker Data](https://www.kaggle.com/arashnic/fitbit)

It consists of 18 CSV files collected from **30 FitBit users** over a
two-month period from **April 12, 2016 to May 12, 2016**.  
The data was voluntarily submitted via a distributed survey conducted
through **Amazon Mechanical Turk**.

For this analysis, a combination of **11 key CSV files** is selected to
enable a more holistic and comprehensive evaluation of user behaviour.
These files cover various health and fitness metrics:

<table class="table" style="width: auto !important; ">
<caption>
Selected CSV Files and Their Content
</caption>
<thead>
<tr>
<th style="text-align:left;">
Selected.CSV.Files
</th>
<th style="text-align:left;">
Content.Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
dailyActivity\_merged.csv
</td>
<td style="text-align:left;">
Daily summary: steps, calories, activity intensity
</td>
</tr>
<tr>
<td style="text-align:left;">
dailyCalories\_merged.csv
</td>
<td style="text-align:left;">
Daily calories burned
</td>
</tr>
<tr>
<td style="text-align:left;">
dailyIntensities\_merged.csv
</td>
<td style="text-align:left;">
Daily intensity breakdown: sedentary to very active
</td>
</tr>
<tr>
<td style="text-align:left;">
dailySteps\_merged.csv
</td>
<td style="text-align:left;">
Daily steps taken
</td>
</tr>
<tr>
<td style="text-align:left;">
heartrate\_seconds\_merged.csv
</td>
<td style="text-align:left;">
Second-level heart rate data
</td>
</tr>
<tr>
<td style="text-align:left;">
minuteCaloriesNarrow\_merged.csv
</td>
<td style="text-align:left;">
Minute-level calorie burn
</td>
</tr>
<tr>
<td style="text-align:left;">
minuteIntensitiesNarrow\_merged.csv
</td>
<td style="text-align:left;">
Minute-level activity intensity
</td>
</tr>
<tr>
<td style="text-align:left;">
minuteStepsNarrow\_merged.csv
</td>
<td style="text-align:left;">
Minute-level steps taken
</td>
</tr>
<tr>
<td style="text-align:left;">
sleepDay\_merged.csv
</td>
<td style="text-align:left;">
Daily sleep duration and efficiency
</td>
</tr>
<tr>
<td style="text-align:left;">
weightLogInfo\_merged.csv
</td>
<td style="text-align:left;">
Weight, BMI, fat percentage, manual vs. auto-recorded
</td>
</tr>
<tr>
<td style="text-align:left;">
minuteMETsNarrow\_merged.csv
</td>
<td style="text-align:left;">
Minute-level metabolic equivalents (METs)
</td>
</tr>
</tbody>
</table>

This multi-table approach allows for a richer exploration of how
activity, sleep, and heart rate metrics interact across different time
resolutions (daily, minute, and second levels).

------------------------------------------------------------------------

#### 2.2 ROCCC Data Quality Assessment

Using the ROCCC framework **(Reliable, Original, Comprehensive, Current,
and Cited)**, the dataset quality is evaluated as follows:

<table class="table" style="width: auto !important; ">
<caption>
ROCCC Data Quality Assessment
</caption>
<thead>
<tr>
<th style="text-align:left;">
ROCCC.Criteria
</th>
<th style="text-align:left;">
Evaluation
</th>
<th style="text-align:left;">
Details
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
Reliable
</td>
<td style="text-align:left;">
Low
</td>
<td style="text-align:left;">
Only 30 users; some files have fewer records. Varying data completeness
and source reliability.
</td>
</tr>
<tr>
<td style="text-align:left;">
Original
</td>
<td style="text-align:left;">
Low
</td>
<td style="text-align:left;">
Data collected through a third-party platform (Amazon Mechanical Turk).
</td>
</tr>
<tr>
<td style="text-align:left;">
Comprehensive
</td>
<td style="text-align:left;">
Medium–High
</td>
<td style="text-align:left;">
Multiple dimensions covered (activity, sleep, heart rate, weight). Some
missingness, especially in sleep and weight.
</td>
</tr>
<tr>
<td style="text-align:left;">
Current
</td>
<td style="text-align:left;">
Low
</td>
<td style="text-align:left;">
Data is from 2016; fitness habits, device accuracy, and lifestyle trends
have likely changed.
</td>
</tr>
<tr>
<td style="text-align:left;">
Cited
</td>
<td style="text-align:left;">
Low
</td>
<td style="text-align:left;">
Third-party source with limited transparency on collection methods.
</td>
</tr>
</tbody>
</table>

**Conclusion:** While the data is not optimal for making final business
decisions, it provides an excellent sandbox for showcasing data
manipulation, integration, and analysis skills.

<hr>

#### 2.3 Data Limitations and Considerations

-   **Small sample size:** While *n* ≈ 30 is statistically acceptable
    for some analyses, it is not representative of the broader
    population.
-   **User coverage is inconsistent:**
    -   Daily activity: 33 unique users
    -   Sleep: 24 users
    -   Weight: Only 8 users, with 5 manually entered
-   **Temporal skew:** Data is clustered mostly between Tuesdays and
    Thursdays
-   **Incomplete tracking:** Not all users recorded all metrics, and
    some metrics are sparsely populated
-   **Outdated data:** Collected in 2016, thus not aligned with current
    user behavior or Bellabeat’s newer technology
-   **Survey-based:** Cannot verify the accuracy or honesty of user
    tracking and self-entry (especially weight)

<hr>

#### 2.4 Data Selection Rationale

Rather than relying on a single CSV, this analysis utilizes **11
integrated files** to:

-   **Enhance depth:** Combining minute-, daily-, and second-level data
    allows for multi-resolution insights
-   **Showcase ETL and data-wrangling skills:** Merging on Id,
    timestamps, and dates enables practice with joins, reshaping, and
    data cleaning
-   **Support exploratory and diagnostic analysis:** Useful for
    hypothesis generation, pattern detection, and visualization
-   **Align with Bellabeat’s interest in holistic wellness:**
    Integrating physical activity, heart rate, sleep, and weight data
    creates a complete user profile

<hr>

### Step 3. Process

We are using R to prepare and process the data. To see my SQL version
[CLICK HERE](https://github.com/emmalacey14/CapstoneProject)

<hr>

#### 3.1 Load Required Libraries

The following R packages were used to support data import,
transformation, and cleaning:

    library(dplyr)       # Data manipulation
    library(tidyverse)   # Wrangling and plotting
    library(readr)       # Reading CSV files
    library(janitor)     # Clean column names
    library(lubridate)   # Dates and times
    library(hms)         # Time-of-day data

<hr>

#### 3.2 Import Raw Files

All .csv files in the Fitabase Data 4.12.16–5.11.16 folder were loaded
into a named list of tibbles for consistency and batch processing.

    fitbit_path <- "Fitabase Data 4.12.16-5.11.16"

    fitbit_data <- list.files(path = fitbit_path, pattern = "*.csv", full.names = TRUE) %>%
      set_names(~ basename(.) %>% tools::file_path_sans_ext()) %>%
      map(read_csv)

    # Optional: Check files were imported
    list.files(fitbit_path, pattern = "*.csv")

<hr>

#### 3.3 Standardise Dataset Names

To improve consistency and readability, the datasets were renamed using
`snake_case` and stripped of unnecessary suffixes like `_merged`.

    # Remove suffix and apply lowercase
    names(fitbit_data) <- names(fitbit_data) %>%
      sub("_merged$", "", .) %>%
      tolower()

    # Rename for clarity and consistency
    rename_map <- c(
      dailyactivity = "daily_activity",
      minutesleep = "minute_sleep",
      sleepday = "sleep_day",
      weightloginfo = "weight_log_info",
      minutecaloriesnarrow = "minute_calories_narrow",
      minuteintensitiesnarrow = "minute_intensities_narrow",
      minutemetsnarrow = "minute_mets_narrow",
      minutestepsnarrow = "minute_steps_narrow",
      hourlycalories = "hourly_calories",
      hourlysteps = "hourly_steps",
      hourlyintensities = "hourly_intensities"
    )

    # Apply mapping
    names(fitbit_data) <- ifelse(names(fitbit_data) %in% names(rename_map),
                                 rename_map[names(fitbit_data)],
                                 names(fitbit_data))

<hr>

#### 3.4 Remove Redundant Datasets

To avoid duplication and streamline analysis, outdated or overlapping
datasets were safely removed:

    old_names_to_remove <- c(
      "dailycalories", "dailyintensities", "dailysteps", "dailyactivity",
      "minutesleep", "sleepday", "weightloginfo", "hourlycalories", "hourlysteps"
    )

    fitbit_data <- fitbit_data[!names(fitbit_data) %in% old_names_to_remove]

------------------------------------------------------------------------

#### 3.5 Merge Time-Series Data

Separate hourly and minute-level datasets were combined into unified
tables by shared keys (`Id`, `ActivityHour`, or `ActivityMinute`).

    # Merge hourly data
    hourly_activity <- fitbit_data$hourly_calories %>%
      inner_join(fitbit_data$hourly_intensities, by = c("Id", "ActivityHour")) %>%
      inner_join(fitbit_data$hourly_steps, by = c("Id", "ActivityHour"))

    # Function to merge multiple narrow datasets
    safe_merge <- function(dfs, by_cols) {
      dfs <- keep(dfs, ~ !is.null(.x))
      reduce(dfs, inner_join, by = by_cols)
    }

    # Merge minute-level narrow data
    minute_narrow_dfs <- fitbit_data[c("minute_calories_narrow", "minute_intensities_narrow", 
                                       "minute_mets_narrow", "minute_steps_narrow")]

    fitbit_data$minute_activity_narrow <- safe_merge(minute_narrow_dfs, by_cols = c("Id", "ActivityMinute"))

------------------------------------------------------------------------

#### 3.6 Merge Sleep, Daily, and Weight Data

Sleep activity, daily activity, and weight information datasets were
combined into a unified table keyed by Id. A full outer join ensures all
user records are preserved.

    # Merge sleep and daily activity data by Id (full outer join)
    combined_data <- merge(sleep_activity, daily_activity, by = "Id", all = TRUE)

    # Merge the combined data with weight information (full outer join)
    combined_data <- merge(combined_data, weight_info, by = "Id", all = TRUE)

    # Check number of unique users after merging
    n_distinct(combined_data$Id)

<hr>

#### 3.7 Clean Columns and Remove Duplicates

All column names were standardsed and duplicate rows removed across the
entire dataset collection.

    # Clean column names across all datasets
    fitbit_data <- lapply(fitbit_data, janitor::clean_names)

    # Remove duplicates
    fitbit_data <- lapply(fitbit_data, function(df) {
      df[!duplicated(df), ]
    })

    # Also apply to merged datasets
    hourly_activity <- hourly_activity %>% distinct()
    fitbit_data$minute_activity_narrow <- fitbit_data$minute_activity_narrow %>% distinct()
    combined_data <-combined_data %>% distinct()

------------------------------------------------------------------------

#### 3.8 Verify Cleaned Datasets

A final check ensures all datasets were correctly renamed and retained
for further exploration.

<hr>

### Step 4. Analyse

I am using R again to do my analysis, to see my SQL versions [CLICK
HERE](https://github.com/emmalacey14/CapstoneProject)

<hr>

#### 4.1 Data summary

Check min, max, mean, median and any outliers. Users average about 63 kg
in weight with a BMI of 24 and burn around 2,100 calories daily. They
take roughly 10,200 steps per day, with a maximum of 36,000 steps. Most
of their time is sedentary (around 12 hours), with only about 30–40
minutes spent in fairly or very active movement. They typically get
about 7 hours of sleep each night.

    combined_data %>%
      dplyr::select(
        ActivityDate,
        TotalSteps,
        TotalDistance,
        VeryActiveMinutes,
        FairlyActiveMinutes,
        LightlyActiveMinutes,
        SedentaryMinutes,
        Calories,
        TotalMinutesAsleep,
        TotalTimeInBed,
        WeightKg,
        BMI
      ) %>%
      summary()

<img width="739" alt="code_1" src="https://github.com/user-attachments/assets/0754583f-671f-4aa6-a75d-2f75f8487c53" />


<hr>

#### 4.2 Activity breakdown

Percentage of active minutes in the four categories: very active, fairly
active, lightly active and sedentary. From the pie chart, we can see
that most users spent 72.5% of their daily activity in sedentary minutes
and only 2.37% in very active minutes.

    library(dplyr)
    library(tidyr)
    library(plotly)

    activity_summary <- combined_data %>%
      summarise(across(c(VeryActiveMinutes, FairlyActiveMinutes, LightlyActiveMinutes, SedentaryMinutes), 
                       ~sum(.x, na.rm = TRUE))) %>%
      pivot_longer(everything(), names_to = "ActivityLevel", values_to = "Minutes") %>%
      mutate(
        TotalMinutes = sum(Minutes),
        Percentage = (Minutes / TotalMinutes) * 100,
        ActivityLevel = recode(ActivityLevel,
                               "VeryActiveMinutes" = "Very Active",
                               "FairlyActiveMinutes" = "Fairly Active",
                               "LightlyActiveMinutes" = "Lightly Active",
                               "SedentaryMinutes" = "Sedentary"))

    plot_ly(
      data = activity_summary,
      labels = ~ActivityLevel,
      values = ~Percentage,
      type = 'pie',
      textposition = 'outside',
      textinfo = 'percent',
      marker = list(colors = c("gold", "darkseagreen", "cornflowerblue", "lavender"))
    ) %>%
      layout(
        title = 'Percentage of Active Minutes by Activity Level',
        showlegend = TRUE
      )

![newplot](https://github.com/user-attachments/assets/6a604d21-13e8-45be-ada7-bc2954d752f4)




<hr>

#### 4.3 Weekly Overview

The bar graph shows that there is a jump on Saturday: user spent LESS
time in sedentary minutes and are MORE active.


<p float="left">
  <img src="https://github.com/user-attachments/assets/a71fd6fe-d305-4cad-823f-dc39f8ba3a44" width="45%" />
  <img src="https://github.com/user-attachments/assets/374c759c-b124-44c7-9d6f-42c511643f20" width="45%" />
</p>


This can be broken down further to show what active type they are
engaging in.

    # Summarise active minutes by weekday and activity type for whole week
    active_breakdown_week <- daily_activity %>%
      group_by(Weekday) %>%
      summarise(
        VeryActive = sum(VeryActiveMinutes, na.rm = TRUE),
        FairlyActive = sum(FairlyActiveMinutes, na.rm = TRUE),
        LightlyActive = sum(LightlyActiveMinutes, na.rm = TRUE)
      ) %>%
      pivot_longer(cols = -Weekday, names_to = "ActivityLevel", values_to = "Minutes")

    # Ensure weekdays are ordered correctly
    weekday_order <- c("Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday")
    active_breakdown_week$Weekday <- factor(active_breakdown_week$Weekday, levels = weekday_order)

![final](https://github.com/user-attachments/assets/c5bb7022-81b5-4b84-b22e-339fcd4f1c34)


<hr>

#### 4.4 Steps Overview

Looking at ‘Total Steps’ we can see when users are most active. From 5PM
to 7PM the users take the most steps.

    ggplot(steps_by_hour, aes(x = factor(Hour), y = TotalSteps, fill = factor(Hour))) +
      geom_bar(stat = "identity") +
      scale_fill_discrete_qualitative(palette = "Pastel 1", n = length(unique(steps_by_hour$Hour))) +
      scale_y_continuous(labels = comma) +  # <- this disables scientific notation
      labs(title = "Total Steps per Hour",
           x = "Hour of Day (24-hour)",
           y = "Total Steps") +
      theme_minimal()

![steps_hour](https://github.com/user-attachments/assets/7d4b6db8-4305-4e5b-8994-804ffa6876a1)

Or our data can be presented in a line chart:

    library(ggplot2)

    ggplot(steps_by_hour, aes(x = Hour, y = TotalSteps)) +
      geom_line(color = "lightblue1",size = 2) +
      geom_point(color = "pink", size=4) +
      scale_y_continuous(labels = scales::comma_format()) +
      labs(title = "Total Steps by Hour of Day",
           x = "Hour (24-hour format)",
           y = "Total Steps") +
      theme_minimal()

![steps_line_2](https://github.com/user-attachments/assets/1362340f-caf3-4579-98ec-f26deac8a4ab)

Lets look at step count per day. Users take the most steps on Tuesdays,
the amount of steps taken slowly decreases throughout the week and then
spikes again on Saturdays.

![steps_week](https://github.com/user-attachments/assets/9bd2f900-68af-4635-84a6-9eedd4a05e51)

We can also look at how many steps are been taken during each activity
type.

    ggplot(long_activity_active, aes(x = TotalSteps, y = Minutes, color = ActivityType)) +
      geom_point(alpha = 0.5) +
      geom_smooth(method = "loess", se = FALSE) +  # trend line only, no confidence interval
      labs(
        title = "Activity Minutes vs Total Steps by Activity Type with Trend Lines",
        x = "Total Steps",
        y = "Minutes of Activity",
        color = "Activity Type"
      ) +
      theme_minimal() +
      scale_color_brewer(palette = "Accent")

![step_active](https://github.com/user-attachments/assets/99edfe7c-4383-42c5-95e8-0a1cd109508b)

This shows us that most steps are being taken during the ‘light’
activity type.

<hr>

#### 4.5 Burning Calories

Lets look at the relationship between activity vs calories.

<p float="left">
  <img src="https://github.com/user-attachments/assets/4fb22fd6-7a8d-44cd-9fea-57cf5ac84491" width="45%" />
  <img src="https://github.com/user-attachments/assets/5e1c6518-c497-403f-9b09-65ab21458286" width="45%" />
</p>


On average, those in a ‘fairly active’ or ‘very active’ phase burn more
calories per minute than those in ‘lightly active’ or ‘sedentary’ phase.

<hr>

Lets see if there is any correlation between sleep and calories - does
increased sleep mean burning less calories?

    ggplot(combined_data, aes(x = TotalMinutesAsleep, y = Calories)) +
      stat_binhex(bins = 30) +
      scale_fill_gradient(low = "lightblue", high = "darkblue") +
      labs(
        title = "Hexbin Plot: Sleep vs Calories",
        x = "Total Minutes Asleep",
        y = "Calories Burned",
        fill = "Count"
      ) +
      theme_minimal()

![sleep_cal](https://github.com/user-attachments/assets/fb7e7a7a-44dd-4feb-9600-2c6ffd6683a6)

The chart doesn’t show us much, so lets check with a correlation test:

    cor_test <- cor.test(combined_data$TotalMinutesAsleep, combined_data$Calories, use = "complete.obs")
    cor_test$estimate  # Shows Pearson correlation

    -0.01769069 

The number is very close to 0, so there’s almost no linear correlation.

<hr>

#### 4.6 Sleep

According to the article: [Fitbit Sleep
Study](https://store.google.com/intl/en/ideas/articles/sleep-study/), 55
minutes are spent awake in bed before going to sleep. We have 13 users
in our dataset who spent over 55 minutes awake before going to sleep.

    awake_55_any_day <- sleepDay_merged %>%
      mutate(AwakeTime = TotalTimeInBed - TotalMinutesAsleep) %>%
      filter(AwakeTime >= 55) %>%
      distinct(Id)

    nrow(awake_55_any_day)

Using our data, we found that the average user is spending 39 minutes
awake before going to sleep. We have 16 users in our dataset spening
over 39 minutes awake before going to sleep.

    average_awake_time <- sleepDay_merged %>%
      mutate(AwakeTime = TotalTimeInBed - TotalMinutesAsleep) %>%
      summarise(AvgAwakeTime = mean(AwakeTime, na.rm = TRUE)) %>%
      pull(AvgAwakeTime)

    cat("Average time spent awake in bed before sleep (minutes):", round(average_awake_time, 2), "\n")

    awake_39_any_day <- sleepDay_merged %>%
      mutate(AwakeTime = TotalTimeInBed - TotalMinutesAsleep) %>%
      filter(AwakeTime >= 39) %>%
      distinct(Id)

    nrow(awake_39_any_day)

<hr>

### Step 6. Act

<hr>

Based on the analysis of user activity data, several clear trends and
opportunities for improving user engagement and health outcomes have
emerged. Below are actionable recommendations Bellabeat can implement:

<hr>

#### User Engagement & Behavior Insights

-   **81% of daily minutes** are spent sedentary; users average only
    **30 fairly/very active minutes** per day.
-   **Peak activity time** is between **5 PM and 7 PM**, suggesting a
    prime window for engagement.
-   **Fridays and Sundays** are notably less active, indicating a drop
    in motivation or energy.
-   Users log minimal data manually, such as **distance and
    weight**—suggesting a preference for **automated tracking**.

<hr>

#### ✅ Actionable Recommendations

##### 🔔 Step Goal Notifications

-   Send real-time reminders of remaining steps around **5–7 PM** to
    help users hit 10,000-step targets.
-   Send motivational prompts **Thursday evening and Friday/Saturday
    mornings** to boost end-of-week activity.

##### 💪 Workout Suggestions Based on Intensity

-   Recommend short, tailored workouts based on current activity level
    (e.g., 10-min moderate session if still sedentary).
-   Suggest higher-intensity activities for users lacking vigorous
    movement.

##### 🎁 Incentive-Based Reward System

-   Offer **credits or unlockable content** (e.g., premium workouts) for
    hitting daily/weekly goals.
-   Replace or supplement badges with **tangible rewards** to improve
    long-term motivation.

##### ⚖️ Improve Data Collection with Automated Tools

-   Market smart devices (e.g., **Bluetooth-enabled scales**) to capture
    weight automatically.
-   Consider phasing out or deemphasizing underused manual entry
    features like distance logging.

##### 📆 Weekend-Focused Activity Campaigns

-   Launch a **“Weekend Recharge”** initiative promoting longer,
    enjoyable activities on Sundays.
-   Provide insights on how even light movement combats sedentary
    behavior.

##### 📈 Expand Data Sources for Future Analysis

-   Incorporate data from additional fitness trackers to explore
    longitudinal user behavior.
-   This would help personalise recommendations and validate patterns
    over time.

##### 😴 Encourage Better Sleep Habits

-   Use devices to detect extended awake periods and prompt users with
    bedtime reminders.
-   Educate users on **sleep quality vs. quantity** to support holistic
    wellness.
