[![Simulation](../../actions/workflows/main.yml/badge.svg)](../../actions/workflows/main.yml)

# Lesson 7 - Quasi-static Loads

The goal of this lesson is to introduce the various ways of simulating loads that vary in time.  The specific learning objectives are the following.

1. How to model buildings.
2. How to model industrial and agricultural loads.
3. How to model public service loads.

## Commercial Buildings

There are many types of commercial buildings that can be modeled in GridLAB-D. The most common are:
- Education
- Grocery
- Healthcare
- Large office
- Restaurant
- Retail
- Small office

## Residential Buildings

There five types of residential buildings:
- Apartment
- Condo
- House
- Lodging
- Townhouse

## Industrial Loads

Industrial loads are identified by their [NAICS code](https://naics.org/)

## Agricultural Loads

TODO

## Public Services

TODO

## Tasks

1. Add a commercial building to load 1
2. Add 4 residential buildings to load 2
3. Add an industrial load to load 4
4. Add an agricultural load to load 5
5. Add a public service load to load 6
6. Use the weather forecast for Denver Colorado
7. Add a general time-varying load to load 7

# Exercices

1. Place meters on all the loads added by tasks 1-5.

# More Information

* [TMY Weather](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Subcommand&doc=/Subcommand/Weather.md)
* [NSRDB Weather](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Utilities&doc=/Utilities/Nsrdb_weather.md)
* [METAR Weather](https://docs.gridlabd.us/)
* [NOAA Weather](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Utilities&doc=/Utilities/Noaa_forecast.md)
