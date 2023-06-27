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

Buildings often use schedules to create time-varying properties. In GridLAB-D schedules are defined using the `schedule` directive, which allows you to specify a time window during which a value is used. The specification of a time window is `MINUTES HOURS DAYS MONTHS WEEKDAYS VALUE;`.  The `MINUTES`, `HOURS`, `DAYS`, `MONTHS`, and `WEEKDAYS` are specified as comma-separated values or ranges, e.g., `1,2,4-6` or `*` for all allowed values. For example the following schedule specifies a daytype weekday value of 22, and a nighttime weekday and weekend value of 18. 

~~~
schedule setpoint
{
    * 7-17 * * 1-5 22.0;
    * 18-6 * * 1-5 18.0;
    * * * * 6-0 18.0;
}
~~~

Commercial building models have many parameters. For details, see the [`building` object documentation](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Building.md)

## Residential Buildings

There five types of residential buildings:
- Apartment
- Condo
- House
- Lodging
- Townhouse

Residential building models are like commercial buildings in that they can have many parameters. For details, see the [`building` object documentation](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Building.md)

## Industrial Loads

Industrial loads are identified by their [NAICS code](https://naics.org/). For details on how to model industrial loads, see the [`industrial` object documentation](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Industrial.md)

## Agricultural Loads

Agricultural loads can be sensitive to different weather variables from buildings.  See the [`agricultural` object documentation](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Agricultural.md) for details.

## Public Services

Public service loads are for street lights and other public services.  They are typically sensitive to daylight and rainfall. See [`public_service` object documentation] for details.

## Tasks

1. Add a commercial building to load 1
2. Add 4 residential buildings to load 2
3. Add an industrial load to load 4
4. Add an agricultural load to load 5
5. Add a public service load to load 6
6. Use the weather forecast for Denver Colorado

# Exercices

1. Place meters on all the loads added by tasks 1-5.

# More Information

* [Building loads](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Building.md)
* [Industrial loads](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Industrial.md)
* [Agricultural loads](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Agricultural.md)
* [Public service loads](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Public_service.md)
