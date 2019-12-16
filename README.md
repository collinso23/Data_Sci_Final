# DataScienceFinalProject
Authored by: Sean Cox, Orion Collins, and Anthony Morganelli

# Introduction

This project is centered around developing a deployment schedule/maintenance window for a Dev Ops team. The idea is to find times that user experience will either not be affected, or minimal interruptions will be experienced. To do this, we will start with the dates and times user 'routines' are played. They function as reminders, for medical and personal purposes. For security reasons, the type of routine can not be included. However, we will simply try to find and visualize the time and day in which the users have no routines running, OR a time when there are the fewest running. The assumption going in is that late at night will be the best time, but we will want to confirm it will not affect customers.

# Selection of Data

Data was aquired using Athena Query on Sean's companies' PostgreSQL database. Personal information needed to be removed for HIPAA compliance. The data has information on when routines will be played. There are a few criteria; day of the week, once on date, monthly on date, yearly on date, and hour and minute to be played. 
The idea is to merge the data in a way so all of the date criteria can overlap, and then times can be applied to dates as needed.

# Methods and Tools

AWS Athena, CSV of query results, numpy, pandas.
Pandas and numpy will be the main technical tools. Constructing a dataframe, and then merging data to construct a calendar of sorts will be step one. 

For visualization, we will want to create a plot to visualize the data to be more eaily viewable. The ideal visualization would be a calendar style plot, with a range of hues to describe the routine density per day. 

# Questionaire

We knew going in that we wanted to construct a Dataframe, and plot it in matplotlib. We will most likely be going with matplotlib.pyplot for our visualization.

# Results / Summary

We found very early (6 am) Saturday morning is the best time to deploy to our servers. This was more or less what we assumed going in, and it confirms that also in the case of our customer base that the least traffic is seen when customers are primarily asleep. A next step to take would be to make sure that whatever routines are meant to run at that time are not crucial customer routines, but that cannot be done in this setting. Visualization is included in the project.

