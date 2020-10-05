# DATA 512 Assignment A1: Data Curation
Author: Aboli Moroney
Date Created: 04-Oct-2020

## Purpose
The goal of this assignment is to construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1, 2008 through August 31, 2020.
All analysis is performed the in the Jupyter notebook and all data, documentation, and code is published in this GitHub repository.

## Data Sources and Licenses
In order to measure Wikipedia traffic from 2008-2020, I have collected data from two different API endpoints, the Legacy Pagecounts API and the Pageviews API.

1.  The Legacy Pagecounts API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts), [endpoint](https://wikimedia.org/api/rest_v1/#!/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end)) provides access to desktop and mobile traffic data from December 2007 through July 2016.
2.  The Pageviews API ([documentation ](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews), [endpoint](https://wikimedia.org/api/rest_v1/#!/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end)) provides access to desktop, mobile web, and mobile app traffic data from July 2015 through last month.

Please find Wikimedia Foundation REST API terms of use [here](https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions)

## Data Files and Code
The following source data files in JSON format contain the raw data fetched from the above APIs: <br>
	1. pagecounts_desktop-site_200801-201607.json <br>
	2. pagecounts_mobile-site_200801-201607.json <br>
	3. pageviews_desktop-site_201507-202008.json <br>
	4. pageviews_mobile-web_201507-202008.json <br>
	5. pageviews_mobile-app_201507-202008.json <br><br>

The final data used for the analysis is saved in a csv file: **en-wikipedia_traffic_200712-202008.csv** <br>

The code for data collection, processing and analysis can be found in the Jupyter Notebook: **data-512-a1-code.ipynb** <br>
*Please refer the LICENSE file with **MIT LICENSE** for understanding the code of conduct*

## Outputs

**1. Final Data CSV File** 
Filename: en-wikipedia_traffic_200712-202008.csv
	Contains: 152 rows of data (excluding headers) ranging from 01 Jan 2008 to 31 Aug 2020. The column headers are as follows:
	year (int64): Year of traffic data <br>
	month (int64): Month of traffic data <br>
	pagecount_all_views (float64): Total page counts (traffic) from legacy API <br>
	pagecount_desktop_views (float64): Desktop page counts (traffic) from legacy API <br>
	pagecount_mobile_views (float64): Mobile page counts (traffic) from legacy API <br>
	pageview_all_views (float64): Total page views from current API <br>
	pageview_desktop_views (float64): Desktop  page views from current API <br>
	pageview_mobile_views (float64): Mobile (web + app) page views from current API <br>


**2. Image of Time Series Chart**
Filename: PageViews_TimeSeries_Plot.png <br>
Contains: A multi-series line chart to show the traffic from different sources (web, mobile and total) over time. <br>

## Caveats
*Data from the Pageview API excludes spiders/crawlers, while data from the Legacy Pagecounts API does not.* <br>
*Data is not available for mobile page counts prior to Oct 2014 hence all values have been set to 0 for those periods.* <br>
*Missing values have been replaced with 0 in the final data csv file.* <br>
