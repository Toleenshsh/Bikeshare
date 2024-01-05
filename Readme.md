## Project Name
Explore US Bikeshare Data

## Resources
 1 Project
 2 Udacity Chat GPT
 3 Stack Overflow
 4 knowledge


## Project overview
In this project, you will use Python to analyze data related to bike share systems in three major cities in the United States: Chicago, New York City, and Washington.














project
import time
import pandas as pd
import numpy as np
CITY_DATA = {'chicago': 'chicago.csv', 'new York City': 'new_york_city.csv', 'washington': 'washington.csv'}
MONTH_DATA = ['all', 'january', 'february', 'march', 'april', 'may', 'june', 'july', 'august', 'september', 'october',
              'november', 'december']
DAY_DATA = ['all', 'monday', 'tuesday', 'wednesday', 'thursday', 'friday', 'saturday', 'sunday']
def get_filters():
    """
     Asks user to specify a city, month, and day to analyze.
     Returns:
        (str) city - name of the city to analyze
        (str) month - name of the month to filter by, or "all" to apply no month filter
        (str) day - name of the day of week to filter by, or "all" to apply no day filter
        """
        print('Hello! Let us explore some US bike_share data!')
    # TO DO:get user input for city (chicago,new york city,washington). HINT: Use a while loop to handle invalid inputs
    # John - moved code around - we always need to ask once then see if we need to try again
    city_name = input(
        "\nWhat is the name of the city to analyze data? (E.g. Input either chicago, new york city, washington\n")
    city_name = city_name.lower()
    while city_name not in CITY_DATA:
        city_name = input(
                "\nPlease try again name of city, input either chicago, new york city, or washington.")
        city_name = city_name.lower()
        ,    while city_name not in CITY_DATA:
        city_name = input(
                "\nPlease try again name of city, input either chicago, new york city, or washington.")
        city_name = city_name.lower()
    # if we get here have a good city_name
    # now do months
    month_name = input(
        "\nwhat month would you like to filter by? January, February, March, April, May, June or type all if you do not have any preference.\n")
    month_name = month_name.lower()
    while month_name not in MONTH_DATA:
        month_name = input(
            "\nSorry i don't understand please try entering a specific month or all again.\n")
        month_name = month_name.lower()
