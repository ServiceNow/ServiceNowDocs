---
title: Completeness Rules by Investigative Case Management Entity Type
description: While most entity record fields are not mandatory, each entity record contains a completeness field that tracks whether the record has sufficient data to be searchable within ICM. The following rules outline the minimum amount of information required for each entity record type to be considered complete.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Investigative Case Management reference, Reference, Public Sector Digital Services \(PSDS\)]
---

# Completeness Rules by Investigative Case Management Entity Type

While most entity record fields are not mandatory, each entity record contains a completeness field that tracks whether the record has sufficient data to be searchable within ICM. The following rules outline the minimum amount of information required for each entity record type to be considered complete.

## Person \(sn\_icm\_person\)

A person entity record is considered complete when all of the following fields are populated:

-   First name
-   Last name
-   Date of birth
-   One of the three identification paths:

    |Path|Required Fields|
    |----|---------------|
    |National Identifier|National identifier + Country of national identifier|
    |Passport|Passport number + Country of passport number|
    |Drivers License|Driver's license number + Driver's license state of issue + Driver's license country of issue|
    | | |


## Organization \(sn\_icm\_organization\)

An organization entity record is considered complete when the following field is populated:

Unique Name.

## Location \(sn\_icm\_location\)

A location entity record is considered complete when all of the following fields are populated:

-   Name
-   Location format
-   Conditional fields based on Location format:

    |Location Format|Required Fields|
    |---------------|---------------|
    |Address|Street address, City, State/Province, Zip/Postal code, Country|
    |GPS Coordinates|Latitude, Longitude|


## Property \(sn\_icm\_property\)

A property entity record is considered complete when at least one of the following fields are populated:

Unique Name OR Serial Number.

## Vehicle \(sn\_icm\_vehicle\)

A vehicle entity record is considered complete when all of the following fields are populated:

-   Short description
-   One of the two identification paths:

    |Path|Required Fields|
    |----|---------------|
    |License Plate|License plate number + State of registration + Country of registration|
    |VIN|VIN|


## Firearm \(sn\_icm\_firearm\)

A firearm entity record is considered complete when **all** of the following fields are populated:

-   Gun make code
-   One of the following:
    -   Serial number
    -   Alternate serial number

