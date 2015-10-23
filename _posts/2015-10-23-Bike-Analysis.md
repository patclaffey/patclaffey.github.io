---
layout: post
title: Personalized Analysis of Cycling Data 
---

Cyclists are well known for our use of technology for performance enhancement.  The materials to build the modern road bike originated in the Formula 1 racing car and fighter jet industries.  The clothing cyclist wear are the most advanced on the planet and orginated from the professional skiing sport.  Cyclist have used bike computers to measure their performance for decades.  Before IoT (Internet of Things), Smart Phones, Apps, FitBits - cyclists have been logging personal activity data and analyzing their performance.  Cyclists have always been at the cutting edge of collecting data for performance improvement - apparently the first device to measure a cycling metric (cadence) was in use in 1895.

I am interested in analysing cycling data to meet requirements from the serious amateur up to the professional athlete. Take the Great Dublin Cycle, a recent 100km sportif cycle around Dublin.  I participated in the event and logged my ride using a Garmin Edge 500 bike computer that recorded time, GPS data, cadence, heart rate and altitude.  You can view the [Garmin dashboard](https://connect.garmin.com/modern/activity/898238015) and also the [Strava dashboard](https://www.strava.com/activities/391934220/overview) for this ride. 
They cater well for the casual or occasional cyclists - the cohorts of weekend warriors.

This is generic out of the box analysis - what the IT profession term as parameterized or "canned" reports.
Every athlete, everywhere in the world, gets exactly the same analysis for a ride.
It is not possible for a performance athlete to get an edge from this analysis - the insights are standardized.
The performance athlete must ask unique questions of themselves and therefor of their performance related data.
So they are blocked.  They have to make do with standard answers to the common questions - and train harder, not smarter.

Today we are training, logging data and uploading it to the "cloud".  We then act as passive consumers of the resulting analysis.  This is our personal data.  We need to take ownership of this data and use this data to drive our sporting performance.  We should be able to ask new and innovative questions of this data - and get the answers we need. Lets get the open source community involved.  To get the ball rolling, and in the spirit of open source, I am making all this code available on GitHub - current code is in [GitHub project branch build.02](https://github.com/patclaffey/docker_jupyter/tree/build.02).  

The platform for this analysis is Python - the programming language and toolkit of the modern data scientist. Despite the familiariy of the cycling variables, it is surprising complex to analyze.  Like a jig-saw puzzle of interlocking parts, everything needs to  fit together to fulfil the bigger picture.  An initial start has been made in building some of these pieces using Python based visualization technologies:
*  [speed / maximum speed calculation](http://htmlpreview.github.io/?https://raw.githubusercontent.com/patclaffey/docker_jupyter/build.03/notebooks/Speed%20Transformation.html) - some of the distance data points from the Garmin computer are outliers and can produce erroneous speed figures.  This notebook applies a time series weighted average algorithm to produce meaningful speed data.
* [time transformation](http://htmlpreview.github.io/?https://raw.githubusercontent.com/patclaffey/docker_jupyter/build.03/notebooks/Time%20Transformation.html).  This shows how the data set is transformed into a classical time series data set.  This opens up the capability of applying the full time series tool-kit to bike data.  This is similiar to the technology used by many Wall Street Quants to analyse stock market data.

In the early days of the automotive industry the Model T car was standardized.  Every customer got exactly the same Model T - right down to the car color.  When Henry Ford was challenged on the this he said that the customer could get any color they wanted "Provided it was Black".  Analytics of cycling data is in exactly the same place today.  Lets give the cyclist choice is how their data is analyzed.
