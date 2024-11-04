# HydroServer Data Model Data Dictionary

This document describes the entities and attributes within the HydroServer data model. 

## Datastream

A Datastream groups a collection of Observations measuring the same ObservedProperty and produced by the same Sensor. Each Datastream represents the properties for a time series of Observations.

| Required | Attribute | Definition | Data Type |
| -------- | --------- | ---------- | --------- |
| M | id | A unique identifier for the datastream. | UUID |
| M |name | A text name for the datastream. Can be auto generated. | String |
| M | description| A text description for the datastream. Can be auto generated | String |
| M | sensorID | Foreign key identifier for the Sensor (method) used to create the Datasteam | UUID |
| M | thingID | Foreign key identifier for the thing on which or at which the Datastream was created. | UUID |
| M | observedPropertyID | Foreign key identifier for the observed property associated with the Datastream | UUID |
| M | unitID | Foreign key identifier for the units of measure in which the Observations within the Datastream are stored | UUID |
| M | observationType | ???? | String |
| M | resultType | ???? | String |
| O | status | A string value indicating the status of data collection/creation for the Datastream. | String |
| M | sampledMedium | The environmental media that is sampled by the Datastream (e.g., air, water, snow, etc.). | Boolean |
| O | valueCount | The number of Observations within the Datastream. | Integer |
| M | noDataValue | A numeric value stored to indicate the absence of data (e.g., -9999). | Float |
| M | processingLevelID | A foreign key identifier indicating the ProcessingLevel for the Datastream | UUID |
| O | intendedTimeSpacing | A numeric value indicating the intended time spacing for Observations within the Datastream. | Float |
| O | intendedTimeSpacingUnits | A foreign key identifier indicating the Units for the intendedTimeSpacing. | UUID |
| M | aggregationStatistic | A string indicating the recorded aggregation statistics for the Datastream (e.g., minimum, maximum, mean, etc.) | String |
| M | timeAggregationInterval | A numeric value indicating the time interval over which recorded Observations were aggregated - i.e., the temporal footprint for each recorded Observation. | Float |
| M | timeAggregationIntervalUnitsID | A foreign key identifier indicating the Units for the timeAggregationInterval. | UUID |
| M | isVisible | An access control flag indicating whether the Datastream metadata is publicly visible. | Boolean |
| M | isDataVisible | An access control flag indicating whether the Observations for the Datastream are visible. | Boolean |
| O | dataSource | A string storing a path to a file from which the Datastream is loaded using the HydroServer Streaming Data Loader software. | String |
| O | dataSourceColumn | A string storing the name of the column in the file from which the Datastream is loaded using the HydroServer Streaming Data Loader software. | String |
| M | archived | A boolean indicating whether the Datastream has been set up to archive to HydroShare or not. | Boolean |
| O | observedArea | The spatial bounding box or spatial extent (point) that belong to the Observations associated with this Datastream. | Object |
| O | phenomenonBeginTime | The Datetime at which the activity began that results in the Datastream's Observations. May be the same as resultBeginTime. | Datetime |
| O | phenomenonEndTime | The Datetime at which the activity ends that results in the Datastream's Observations. May be the same as resultEndTime. | Datetime |
| O | resultBeginTime | The timestamp of the first Observation in the Datastream. | Datetime |
| O | resultEndTime | The timestamp of the last Observation in the Datastream. | Datetime |

## FeatureOfInterest

An Observation results in a value being assigned to a phenomenon. The phenomenon is a property of a feature, the latter being the FeatureOfInterest of the Observation. The FeatureOfInterest may be a real-world feature such as a stream reach, watershed, aquifer, etc. HydroServer treats FeatureOfInterest as an optional entity. The FeatureOfInterest for a Datastream need not be specified.

| Required | Attribute | Definition | Data Type |
| -------- | --------- | ---------- | --------- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

## HistoricalLocation

A Thing’s HistoricalLocation entity set provides the times of the current (i.e., last known) and previous locations of the Thing.

| Required | Attribute | Definition | Data Type |
| -------- | --------- | ---------- | --------- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

## Location

The Location entity locates the Thing. A Thing’s Location entity is defined as the last known location of the Thing.

| Required | Attribute | Definition | Data Type |
| -------- | --------- | ---------- | --------- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

## Observation

An Observation is the act of measuring or otherwise determining the value of a property, including its numeric result and the date/time at which it was observed.

| Required | Attribute | Definition | Data Type |
| -------- | --------- | ---------- | --------- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

## ObservedProperty

An ObservedProperty specifies the phenomenon of an Observation (e.g., flow, temperature, pH, dissolved oxygen concentration, etc.).

| Required | Attribute | Definition | Data Type |
| -------- | --------- | ---------- | --------- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

## Organization

An Organization is a body of people having a particular purpose, in particular a business, agency, research group, research institute, etc. For HydroServer, this is the Organization with which a Person involved in data collection is affiliated.

| Required | Attribute | Definition | Data Type |
| -------- | --------- | ---------- | --------- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

## Person

Individual people who are involved in data collection or who are responsible for observational data stored in the database.

| Required | Attribute | Definition | Data Type |
| -------- | --------- | ---------- | --------- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

## Photo

A photo of a Thing.

| Required | Attribute | Definition | Data Type |
| -------- | --------- | ---------- | --------- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

## ProcessingLevel

The degree of quality control or processing to which a Datastream has been subjected. For example, raw versus quality controlled data.

| Required | Attribute | Definition | Data Type |
| -------- | --------- | ---------- | --------- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

## ResultQualifier

Data qualifying comments added to individual data values to qualify their interpretation or use.

| Required | Attribute | Definition | Data Type |
| -------- | --------- | ---------- | --------- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

## Sensor

A Sensor is an instrument that observes a property or phenomenon with the goal of producing an estimate of the value of the property. A Sensor may also be a method or procedure by which a Datastream is derived or created when no sensor is involved - e.g., discharge derived from stage data using a site-specific rating curve, or daily data derived from 30-minute data through aggregation.

| Required | Attribute | Definition | Data Type |
| -------- | --------- | ---------- | --------- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

## Thing

A thing is an object of the physical world (physical things) or the information world (virtual things) that is capable of being identified and integrated into communication networks. In the context of environmental monitoring and HydroServer, a Thing is a monitoring station (e.g., a streamflow gage, water quality station, weather station, diversion measurement location, etc.).

| Required | Attribute | Definition | Data Type |
| -------- | --------- | ---------- | --------- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

## ThingAssociation

An association between a Thing and the Person or Persons who own and/or manage the information for that Thing. 

| Required | Attribute | Definition | Data Type |
| -------- | --------- | ---------- | --------- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |













Unit