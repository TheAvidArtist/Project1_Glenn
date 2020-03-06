# Project1_Glenn

# Introduction

In this report I will compare information (number of dives, sound of speed profile in day vs night/location, etc) from different CTDs.  They are located off the Pacific Northwest coast and measure salinity, temperature and pressure and from this we were able to extrapolate the speed of sound profile and depth from this data.


| CTD  | Season | Number of Dives |
| ------------- | ------------- | ------------- | 
| Oregon Shelf Surface Piercing Profiler Mooring  | Winter | 2 |
| Oregon Shelf Surface Piercing Profiler Mooring  | Summer | 5 |
| Oregon Offshore Cabled Shallow Profiler Mooring  | Winter | 7 |
| Oregon Offshore Cabled Shallow Profiler Mooring  | Summer | 6 |
| Oregon Offshore Cabled Deep Profiler Mooring  | Winter | 12 |
| Oregon Offshore Cabled Deep Profiler Mooring  | Summer | 2 |
| Oregon Slope Base Shallow Profiler  | Winter | 7 |
| Oregon Slope Base Shallow Profiler  | Summer | 6 |
| Oregon Slope Base Deep Profiler  | Winter | 1 |
| Oregon Slope Base Deep Profiler  | Summer | 4 |
| Axial Base Shallow Profiler  | Winter | 7 |
| Axial Base Shallow Profiler  | Summer | 1 |
| Axial Base Deep Profiler  | Winter | 1 |
| Axial Base Deep Profiler  | Summer | 1 |


# Comparing the number of dives in Winter vs Summer

Barring the first data point, the shallow profiler seems to have more dives per 24 hours.  I would assume this is because there is a lot less ground to cover and if they are moving the same speed the CTD would go up and down more times in the shallow waters

    

Per the code, we can see that in Winter, the highest ssp is 1503m/s from cW5, which corresponds to Oregon Slope Base Deep Profiler. In Summer, the highest ssp is 1510m/s from cS2, which is from the Oregon Offshore Cabled Shallow Profiler.  Since the farther away from the equator (higher latitudes) you get, the colder it gets, water will have a higher density at latitudes further from the equator and therefore a faster speed of sound.



Since I chose the same time frame for each data set (7am to 7am in Pacific Standard Time), the first half of the graph is the day time and the second half is nighttime.  We can see that most the graphs are symmetric, implying that there isn’t much of a difference between the dives in day or night, except in Winter 5 and 6, which corresponds to Oregon Slope Base Deep Profile and Axial Base Shallow Profiler.  In those cases, the CTD only seemed to dive deep during the day.  I would guess that this is because the water is slightly warmer and is less difficult to move through.


For the most part, they are the same shape which shows a general trend.  However, in the summer the speed of sound can increase more near the surface, most likely due to the sun evaporating the surface water and causing a much higher salinity.


# Effect of Location

There isn’t a clear correlation between location and ssp profiles as we can see from the first 14 graphs.  Mostly they seem to follow the same trends of ssp rising in the shallow profilers or falling with the deep profilers, except for the offshore Oregon one.  We should know that the farther we go from the equator, the higher the ssp profiles should go, however, since the water is getting colder and denser.

# Conclusion

It is hard to come to any concrete conclusions as this data does not seem entirely accurate.  It is difficult to tell the difference of information between profilers in day vs night or see the effect of location, which does not seem entirely correct.
