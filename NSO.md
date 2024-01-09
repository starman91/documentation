# High-Resolution Wind and Structural Loads Data measured on Parabolic Trough Solar Collectors at Nevada Solar One (NSO)

## Description

<!--  A brief description of the data including:
- how it was produced?
- why it important/novel
- who/how it might be used -->

This data set characterizes the complex wind conditions and resulting structural loads on full-scale, operational parabolic trough collectors.
Over two years, NREL conducted comprehensive field measurements of the atmospheric turbulent wind conditions and the resulting structural wind loads on the parabolic troughs at the Nevada Solar One plant. The measurement set-up included meteorological masts and structural load sensors on four trough rows.
Additionally, we commissioned a lidar, scanning the horizontal plane over the trough field.

Wind loading is a main contributor to structural design costs of Concentrating Solar Power (CSP) collectors, such as heliostats and parabolic troughs. These structures must resist the mechanical forces generated by turbulent wind. At the same time, the reflector surfaces must exhibit the necessary rigidity to maintain their optimal optical performance in windy conditions. 
Studying wind-driven loads at a full-scale, fully operational CSP plant will provide insights into the wind impact on the solar collector fields, which currently is beyond the capabilities of wind tunnel tests or state-of-the-art simulations.

By providing this first-of-its-kind data set to the CSP community, we aim to enhance the community's understanding of wind-loading experienced by CSP collector structures.
The data set might be used, for example, to verify simulations or for comparisons to wind tunnel tests.

## Directory structure

<!--  If the dataset is made up of multiple files a description of how they are/will
be stored in relation to each other. -->

The directory structure is:

NSO/  <br>
&nbsp; {}/   &emsp;       &emsp; &emsp;     &emsp;        &emsp;    data set type: inflow_mast_1min, inflow_mast_20Hz, wake_masts_1min, wake_masts_20Hz, loads_1min, loads_20Hz, or lidar  <br>
&nbsp;&nbsp;&nbsp;   year={}/     &emsp;    &emsp;  &emsp;        year  <br>
&nbsp;&nbsp;&nbsp;&nbsp;    month={}/     &emsp;   &emsp;        month  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;     day={}/   &emsp;    &emsp;   &emsp;        day  <br>


The structure of the filenames is:

Type_YYYY-MM-DD_00h_to_YYYY-MM-DD_00h.parquet  <br>
YYYY-MM-DD: date of the daily file that contains data from 00:00 UTC to 24:00 UTC  (lidar data contain one scan shorter than a day, so the lidar file name also contains hour and minute)<br>
Type: Inflow_mast_20Hz, Inflow_mast_1min, Wake_masts_20Hz, Wake_masts_1min, Loads_20Hz, Loads_1min, or Lidar  <br>


Examples:

NSO/inflow_mast_20Hz/year=2022/month=02/day=03/Inflow_Mast_20Hz_2022-02-03_00h_to_2022-02-03_23h.parquet<br>
NSO/lidar/year=2023/month=04/day=02/Lidar_2023-04-02_19-00-17_to_2023-04-02_19-00-17.parquet


## Data Format

<!--   How the data is stored with in each file including a data dictionary with
 - dataset/variable/column names
 - units -->

Data are stored in the Parquet file format. The variables and units in each dataset are listed in [1].

## Code Examples

<!-- Example scripts of how to access the data IN THE CLOUD. A jupyter notebook or link to a github repo with examples can be used instead. -->

Example Python scripts to read the data are provided at the OEDI data lake.

## References

[1] Reference to a data paper describing the data set (to be added after publication).