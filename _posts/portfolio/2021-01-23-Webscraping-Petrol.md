---
layout: post
Title: Web Scraping Petrol prices
tags: [Climate, Economics, Time series, Web scraping]
math: true
---
Welcome to Not Pure Poole! This is an example post to show the layout. {: .message }
<img src="https://images.unsplash.com/photo-1578849161904-f141cc69a5f9?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&auto=format&fit=crop&w=630&q=80" class="page-image" alt="">

# Webscraping Petrol prices

## What is this?
This is a small project I made in November of 2020 where I webscrape the webpage bensinpriser.nu for user inputed petrol prices for gas stations (Bensin means 'Petrol' in swedish hence the name). The website doesn't have any way to access it's historical data so I though I'd create one of my own. 
It contains the names and adress of the gas station, colour(which represent the type of user that inputed the price), Price, Date Entered (into the website), and Date Collected (which is when I scraped the website).

## How do I use the project?
### Analysis
For analysis, you would first have to remove all redundant values (which there are alot of).

### How to set it up on your own
If you want to set it up on your own so that it everyday, then the following will explain how you do it on Windows 10, Python 3.8. This guide may be incomplete since I'm working from memory

1) Fork repository
2) Download and install the python packages using pip: 
    - pandas
    - datetime
    - os 
    - urllib.request
    - openpyxl
3) Create or download the files 'lastchecked.txt' and 'Scraped.xlsx'
4) Open up 'Task Scheduler' which is native to windows 10
5) Select 'Task scheduler Library' create a new folder
6) Press 'Create Task'
7) Select 'Windows 10' in 'Configure for:' on the 'General' tab
8) On the 'Triggers' tab, press 'New...' 

    i. Set 'Begin the task:' to 'At log on'

    ii. Tick 'Delay task for:' and set it to '30 seconds'

    iii. Tick 'Enabled'

9) On the 'Actions' tab, press 'New'

    i. In 'Action:' select 'Start a program'

    ii. On the line 'Program/script:' select the python version that you're using. Mine is installed at 'C:\Users\sleep\AppData\Local\Programs\Python\Python39\python.exe'
    
    iii. In 'Add arguments', add 'Bensin_Scraping.py'
    
    iv. In 'Start in', add the folder where you stored 'Bensin_Scraping.py'

That's it!
Everytime you start your computer, the scheduler will start Bensin_Scraping.py which will check if you've scraped that day. If you have, nothing happens. If it hasn't, then it scrapes which will take about 5-10 seconds and conclude by saying how many pages were collected.

## To-do list
[] Remove redundancies before they're added to the main storage file Scraped.xlsx OR have a seperate program that removes redundancies but only when you call on it

[] Introduce Swedish letters to make it more readable

[] Look into and setup an SQL server so you can pull data from the server instead of an excel file.

<a href="https://github.com/Supersoppan/Misc.-Projects/tree/main/Bensin_scraping" target="_blank">You can view the code and associated files here.</a>