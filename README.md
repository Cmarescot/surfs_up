# surfs_up

## Overview:
### Module 
In this analysis we were tasked with exploring weather trends for the island of Oahu to determine if it is a good place to start a Surboard and Ice cream shop.

### Challenge 
In our challenge specifically, we focused on the months of December and June in order to determine if the surf and ice cream shop would be derable all year round. 

## Results:
Our analysis found that:
- As expected the temperates were warmer during the months of December but not by a long shot 
- June had a average (mean) temperature of 74.9 degrees and December had a average of 71.4 degrees
- There were less temperature counts for the month of December which may have played a part in the temperature result differences between the two months 
- June and December's max temps differed only by 2 degrees with the highest in June being 85 degrees and the highest in December being 83 degrees

## Summary:
- In general there were no big diffrences in Temperature between the two months that would substantially change the prospects of the Surfboard and Ice cream shop. 
In general, temperatures stay at around the same degrees. 

Performing these additional queries would help us gather more data on the month of June and December: 
- Perform a query on precipitation for both months. Rain plays a big factor when it comes to surfing and ice cream sales, so knowing more about rain can give us some more information. 
(precipitation_results = session.query(Measurement.date, Measurement.prcp).filter(Measurement.date.regexp_match(month))
- Lastly, we could do a query where we find the activity level (amount of recordered precipitation ) for each station by date. Using the info gathered by each station can let us get insight on weather for locations surrounding those station during these months 
(activity_results = session.query(Measurement.station, Measurement.date, func.count(Measurement.station)).\
group_by(Measurement.station).order_by(func.count(Measurement.station).desc()).all())
