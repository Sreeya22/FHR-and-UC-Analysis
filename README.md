# FHR and UC Analysis
This project involves analyzing Fetal Heart Rate (FHR) and Uterine Contractions (UC) data. The main objectives are to visualize the FHR and UC over time, perform a detailed FHR analysis in time epochs, and detect and analyze UC peaks, particularly those lasting more than 30 seconds.

## Goals

1. **Visualize FHR and UC Over Time:** Create plots to observe trends, peaks, and anomalies.
2. **Detailed FHR Analysis:** Divide data into epochs to gain insights into fetal heart rate.
3. **UC Peak Detection:** Identify peaks in UC data, focusing on those lasting longer than 30 seconds.

## Libraries Used

- **Matplotlib:** For plotting graphs to visualize FHR and UC data.
- **Pandas:** For data manipulation and analysis.
- **NumPy:** For performing mathematical calculations.
- **SciPy:** For detecting peaks and calculating their widths in UC data.

## Project Details

### 1. Plotting FHR and UC Data

- **Purpose:** Visualize the data to observe trends in FHR (beats per minute) and UC (TOCO values).
- **Outputs:**
  - FHR graph displaying heart rate over time.
  - UC graph showing contraction intensity over time.

### 2. FHR Analysis Over Epochs

- **Purpose:** Analyze FHR by dividing the data into epochs (3.75 seconds each).
- **Outputs:**
  - Average FHR values (bpm) for each epoch.
  - Pulse intervals (in milliseconds) for each epoch, calculated using the formula:
    \[
    \text{Pulse Interval} = \frac{60,000}{\text{Average FHR in bpm}}
    \]

### 3. UC Peak Detection

- **Purpose:** Detect peaks in UC data to identify contractions and measure their widths.
- **Outputs:**
  - List of peak widths in seconds for each detected peak.
  - Count of peaks lasting longer than 30 seconds.
  - Average duration of these wide peaks.

### 4. Handling Edge Cases (No Wide Peaks Detected)

- **Purpose:** Manage cases where no wide peaks are detected to prevent errors during average duration calculations.
- **Outputs:**
  - Number of wide peaks detected.
  - Average duration of wide peaks or a message indicating none were found.

## Results

- **Number of peaks wider than 30 seconds:** 4
- **Average duration of peaks wider than 30 seconds:** 181.375 samples

## Installation

To run this project, ensure you have the following libraries installed:

```bash
pip install matplotlib pandas numpy scipy
```

## Usage

Run the analysis script to visualize data, analyze FHR, and detect UC peaks. Make sure to have the FHR and UC data available in the correct format.
