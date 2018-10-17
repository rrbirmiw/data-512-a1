# README

## Purpose 

The goal for this assignment is to construct, analyze, and publish a dataset of monthly English Wikipedia mobile and desktop page traffic from the earliest month where data is available through the most recent month where data is available. (Jonathan Morgan, Os Keyes. HCDE 512. Lecture 3. University of Washington. 2018). The Wikipedia traffic data stems from two sources, discussed below. These two sources are appropriately joined together to produce the final composite data set. A monthly time-series visualization is also produced, showing the evolution of traffic for each of the various Wikipedia "access-points"/access-sites -- mobile app, mobile web, desktop -- for each of the two APIs used. 

*https://wiki.communitydata.cc/Human_Centered_Data_Science_(Fall_2018)/Assignments#A1:_Data_curation*

## Data Sources

*Data was gathered from the Wikimedia REST API, Wikimedia Foundation, 2018. CC-BY-SA 3.0*

Data for this project was gathered from two Wikimedia REST APIs: 
  1. Pagecounts API 
  2. Pageviews API 
  
Python's `requests` library is used to pull the JSON data from each of these two RESTful APIs. 
  
#### Pagecounts API 
https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts

The Pagecounts is a *Legacy* API, is no longer updated. The data is filterable by access-type (desktop or mobile). Data is availble from Dec 2007 to mid 2016 (desktop) and Oct 2014 to mid 2016 (mobile). The Pagecounts API does not filter our web-crawlers, so data here is not necessarily "organic" traffic. 

#### Pageviews API
https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews

Developed to replace the Legacy Pagecounts API, has mobile and desktop data from mid 2015 to the present. The data is more granular; with respect to this project, filterable by three access-types: mobile-web, mobile-app, and desktop. The data is also filterable by "true" (organic) traffic users, and also all traffic (even containing crawlers, etc.). Unliked the former API, this API is still being maintained. 

