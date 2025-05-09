# Benchmark Instances for EOSSP-MRT

This repository contains the benchmark instances used in the study titled  
**"Earth Observation Satellite Scheduling Problem for Multitemporal Revisit Tasks: A Variable Neighborhood Search Algorithm"**  
*(Manuscript currently under review.)*

These instances are made publicly available to support reproducibility and to encourage further research on Earth observation satellite scheduling problems with multitemporal revisit tasks.

---

## 📁 Repository Structure

- **`DataSummary.xlsx`**  
  A summary file that contains the complete dataset from which all test instances are generated. It includes:
  - `Tasks`: All candidate observation tasks
  - `Satellites`: All candidate satellites
  - `TaskTimeWins`: All visibility time windows between satellites and targets
  - `DownloadTimeWins`: All data download time windows between satellites and ground stations

- **`S1/` to `S18/`, `U1/` to `U18/`**  
  A total of **36 instance folders**, each corresponding to an instance tested in the study. Each folder includes four text files:

  ### `Satellites.txt`

  - **Line 1**:  
    ```
    the number of satellites: N
    ```
  - **Lines 2 to N+1**:  
    ```
    satellite_id,max_storage,transition_time
    ```

  ### `Tasks.txt`
  - **Line 1**:  
    ```
    the number of tasks: M
    ```
  - **Lines 2 to M+1**:  
    ```
    task_id,longitude,latitude,revisit_count,ideal_time_1%tolerance_1%fixed_profit_1%variable_profit_1|ideal_time_2%tolerance_2%fixed_profit_2%variable_profit_2|...
    ```

  ### `TaskTimeWins.txt`
  - **Line 1**:  
    ```
    the number of TaskTimeWins: T
    ```
  - **Lines 2 to T+1**:  
    ```
    satellite_id,task_id,start_time,end_time
    ```

  ### `DownloadTimeWins.txt`
  - **Line 1**:  
    ```
    the number of Download Time Windows: D
    ```
  - **Lines 2 to D+1**:  
    ```
    satellite_id,ground_station_id,ground_station_name,start_time,end_time
    ```

---
## 📌 Notes

- All underlying data (task attributes, visibility windows, and download opportunities) are generated through simulation using relevant software.
- All 36 instances are constructed by selecting subsets of satellites and tasks from the full dataset in `DataSummary.xlsx`.
---
