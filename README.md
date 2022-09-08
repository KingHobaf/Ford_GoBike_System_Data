### Dataset

Ford GoBike System Data is a dataset that contains different rider in different categories which are in genders, users, starting and ending locations. The location makes it possible to get distance travelled and gave room for analysis. However, the NaN values were dropped because the are really very small. The Ford GoBike was downloaded from the link: https://s3.amazonaws.com/fordgobike-data/index.html

### Summary of findings
The project is a dataset that is messy, the dataset was wrangled and visualized. It was also discovered that the more the variable the better  the prediction and the duration of rides, changes as the we checked from univariate to bivariate to multivariate.

#### The following issues were discovered and clean in the analysis:
### Identifying the Quality and Tidiness issues

## Issues
Quality Issues

- Check for the columns with null or missing values and drop them all
- The distance covered by each bike cannot be deduced. So craete another variable called distance and calculate the distance covered by each bike from the Lattitude and longitude variables.
- Change the datatype of start_time and end_time to datetime and member_birth_year to integer
- Rename columns for better representation
- Drop the outlier in the duration_sec column
- Drop all unnecessary columns, columns not needed

Tidiness Issues: Feature Engineering
- Get the month, weekday and day from the start_time column
- Get the age of the riders from birth_year into a column called age
- Deduce the how long in mins it takes for each biker to ride a bike

## The structure of the dataset is as follows:
> - Prior to the data wrangling (assessing forr issues and cleaning of data) there were 183412 riders with 16 features/characteristics, giving the information about each biker. These features are ['duration_sec', 'start_time', 'end_time', 'start_station_id', 'start_station_name', 'start_station_latitude', 'start_station_longitude', 'end_station_id','end_station_name', 'end_station_latitude', 'end_station_longitude', 'bike_id', 'user_type','member_birth_year', 'member_gender', 'bike_share_for_all_trip']
> - However, after the data wrangling, some features were removed from the dataset ['start_station_id', 'end_station_id', 'bike_id'] and the dataset now contain information of 172638 bikers with 19 features/characteristics describing each biker.
> - Featured engineering was performed on some of the features and they were added to the remaining features. These engineered variables are age, month, distance_km, weekday, day, duration_min.

#### The following are some of the insights gotten in the course of the visualization:
> - Because weekdays are in view, the users spent more times on trips on Saturday and Sundays
> - Considering genders, weekdays and duration, the time spent by male and female are almost the same while that of others seems different
> - Female spend more time on trips compared to male, considering user_type.
> - Distance and duration have positive correlatio
