# Measurement Data

DWRi currently retrieves and stores water measurement data from hundreds of measurement locations throughout the state of Utah. These data are either collected by DWRi using dataloggers, sensors, and telemetry systems managed by DWRi or are retrieved ("scraped") from various different data providers. Data consist of time series of water flows that are collected at varying time resolutions, but that are then aggregated to daily timesteps for use in water distribution accounting.

DWRi currently stores and manages these data within a relational database called "DIVRT", which is implemented using Microsoft SQL Server. As part of DWRi's system modernization work, measurement data are being transitioned to a new software system called "HydroServer". HydroServer uses a relational database implemented in PostgreSQL to store measurement data.

The information/data models used by both of these systems are documented here:

* DWRi DIVRT database data model
* [HydroServer database data model](hydroserver/)
