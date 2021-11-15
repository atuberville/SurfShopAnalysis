# SurfShopAnalysis
## Purpose
The purpose of this analysis was to determine the average temperatures for the months of June and December to decide if a dual-purpose surf and ice cream shop might be successful on the island of Oahu throughout the year. 
## Differences
- There are significantly less data points for the month of December vs. the month of June. This could be because the weather station data was not available for a given date however, there are no null values in either data set.
- The minimum temperature in December is 8 degrees less than June. The different percentiles from both months only vary by 4 degrees or less; meaning there is very little temperature fluctuation between days and the temperature on the island doesn’t vary much or often.
- The maximum value in June is only 2 degrees higher than December, with the smaller value being 83 degrees. That’s probably great news for an ice cream shop!
## Summary
Temperatures on the island of Ohau are consistent and easily to track, I think a better picture would be formed if we looked at the data from year to year to see if there are some years where the temperatures show a different trend between June and December. 

start_date = '2017-06-01' 
end_date = '2017-06-30'
month_of_changedate = session.query(func.min(Measurement.tobs), func.max(Measurement.tobs), func.avg(Measurement.tobs)).\
filter(Measurement.date >= start_date).\
filter(Measurement.date <=end_date).all()
print(month_of_changedate)

I would also recommend viewing data by tower in order to determine if one part of the island would be more favorable than the other. 
