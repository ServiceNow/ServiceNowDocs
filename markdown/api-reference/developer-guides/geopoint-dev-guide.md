---
title: GlideGeoPoint Developer Guide
description: The GlideGeoPoint developer guide contains information about how to compute distances between latitude and longitude values \(geopoints\), return locations within given geopoint and radius values, and use additional functionality provided by supported GlideGeoPoint API functions.Use the GlideGeoPoint API to insert new records and create new geopoints.Use the getDisplayValue\(\) GlideGeoPoint API function to read all geopoint values from a specific table.Use the distance\_sphere glide function to return the distance between geopoints in meters.Use the DISTANCE\_SPHERE\_WITHIN query condition to filter for records having a geopoint value within the radius of a defined latitude, longitude point. 
locale: en-US
release: xanadu
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Developer guides, API implementation and reference]
---

# GlideGeoPoint Developer Guide

The GlideGeoPoint developer guide contains information about how to compute distances between latitude and longitude values \(geopoints\), return locations within given geopoint and radius values, and use additional functionality provided by supported GlideGeoPoint API functions.

The [Geo point field type](https://www.servicenow.com/docs/access?context=geo-point-field-type&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) allows you to store a latitude and longitude pair in a single field. Geopoints can be useful anytime you want to store a geographical point of interest, to ask how far a part two points of interest are from one another, or to search for all points within a certain distance from another point. For example, you can use geopoint functionality to quickly determine all of your customer's delivery locations and then adjust delivery fees based on their distance from the store.

Key aspects of the geotype data type are:

-   It consists of a pair of decimal numbers representing longitude and latitude values.
-   The range for longitude is \(-180, 180\]. Any value outside this range is normalized to the equivalent value inside this range.
-   The range for latitude is \[-90, 90\]. Any value outside this range is normalized to the equivalent value inside this range.
-   Geopoint values are always accepted as input and display as a comma-separated pair: “longitude,latitude”. Parentheses may optionally surround the expression.
-   Both longitude and latitude values are stored up to 6 decimal places of precision.

For more information about the geopoint data type, see [Function field](https://www.servicenow.com/docs/access?context=platform-support-functions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

The examples in this guide assume that a custom table, `u_geopoint`, is populated with fields `u_name` and `u_location`, where `u_name` is of type 'string' and lists the names of major cities and `u_location` is of type 'geopoint' and lists the latitude/longitude points of each city respectively.

## Create geopoints using the GlideGeoPoint API

Use the GlideGeoPoint API to insert new records and create new geopoints.

The [GlideGeoPoint - Global](../../../../app-store/dev_portal/API_reference/GlideGeoPoint/concept/GlideGeopointGlobalAPI.md#) API allows you to set and retrieve geopoint values. However, you can perform additional functionality to insert new records by setting geopoints directly in a script using string notation or a GlideGeoPoint object.

-   **Inserting a new record using string notation.**

    Set the value of the geopoint field `u_location` using a string. The string consists of a comma-delimited pair of longitude and latitude values. The following example shows how to set a new geopoint in the `u_geopoint` table using string notation.

    **Note:** GlideGeoPoint API values are always listed in longitude, latitude order.

    ```
    const longitude = "-87.628018"; 
    const latitude = "41.885778"; 
    const geopoint = longitude + "," + latitude; 
     
    const myGeoPoint = new GlideRecord("u_geopoint"); 
    myGeoPoint.initialize(); 
    myGeoPoint.setValue("u_name", "Chicago"); 
    myGeoPoint.setValue("u_location", geopoint); 
    myGeoPoint.insert();
    ```

-   **Inserting a new record using the GlideGeoPoint object.**

    Set the value of the geopoint field `u_location` using a GlideGeoPoint object.

    ```
    const longitude = -87.628018; 
    const latitude = 41.885778; 
    const geopoint = new GlideGeoPoint(longitude, latitude); 
     
    const myGeoPoint = new GlideRecord("u_geopoint"); 
    myGeoPoint.initialize(); 
    myGeoPoint.setValue("u_name", "Chicago"); 
    myGeoPoint.setValue("u_location", geopoint); 
    myGeoPoint.insert();
    ```


## Read geopoint values using the GlideGeoPoint API

Use the getDisplayValue\(\) GlideGeoPoint API function to read all geopoint values from a specific table.

The standard GlideGeoPoint API allows you to retrieve a geopoint value via the [GlideGeoPoint - getDisplayValue\(\)](../../../../app-store/dev_portal/API_reference/GlideGeoPoint/concept/GlideGeopointGlobalAPI.md#) function. However, it is possible to read all geopoints defined in an entire table. The following example script demonstrates how to use the getDisplayValue\(\) function to retrieve all records from the `u_geopoint` table, which includes the `u_location` field of type 'geopoint'. You can this example script and adjust it to your own specific use case.

**Note:** GlideGeoPoint API values are always listed in longitude, latitude order.

```
const myGeoPoint = new GlideRecord("u_geopoint"); 
myGeoPoint.query(); 
 
while (gr.next()) 
  gs.info("Name: {0}  Location: {1}",  
    myGeoPoint.getDisplayValue('u_name'),  
    myGeoPoint.getDisplayValue('u_location'));
```

The output returns all records in the `u_geopoint` table. The display value of a geopoint includes the longitude followed by the latitude, separated by a comma and surrounded in parentheses.

```
Name: London  Location: (-0.189937, 51.473584) 
Name: Puerto Rico  Location: (-66.561301, 18.291136) 
Name: Glasgow  Location: (-4.223964, 55.867846) 
Name: Chicago  Location: (-87.628018, 41.885778) 
Name: Tasmania  Location: (146.757677, -42.173578) 
Name: Bermuda  Location: (-64.761595, 32.315798) 
Name: Miami  Location: (-80.206458, 25.767242) 
Name: Sydney  Location: (151.205230, -33.890115) 
Name: Perth  Location: (115.871253, -31.971583) 
Name: Dublin  Location: (-6.304994, 53.348317)
```

## Calculate the distance between two geopoints

Use the `distance_sphere` glide function to return the distance between geopoints in meters.

The geopoint glide function, `distance_sphere`, allows you to compute the distance between two geopoints. The function returns the distance in meters. `distance_sphere` can be used in the definition of a function field element on a table or via a script. Three syntaxes are supported and all parameters are required:

-   `glidefunction:distance_sphere(geopoint1, geopoint2)`
-   `glidefunction:distance_sphere(geopoint1, longitude2, latitude2)`
-   `glidefunction:distance_sphere(longitude1, latitude1, longitude2, latitude2)`

When using these syntaxes, note that:

-   geopoint1 and geopoint2 are table elements of type 'geopoint'
-   longitude1, longitude 2, latitude 1, latitude 2 are numerical table elements or constants
-   In all cases, the return value of this function is a decimal representing the distance between two geopoints in meters

The following example script defines a `distance_sphere` function to compute the distance between all geopoints stored in the `u_location` field of the `u_geopoint` table and the point `-0.189937` longitude, `51.473584` latitude \(which is roughly the location of London\). The function is added to the GlideRecord query to produce results.

```
const distToLondon =  
"glidefunction:distance_sphere(u_location, '-0.189937', '51.473584')"; 
 
const myGeoPoint = new GlideRecord('u_geopoint'); 
gr.addFunction(distToLondon); 
gr.query(); 
 
while(myGeoPoint.next()) 
  gs.info("Name: {0}  Dist to London(m): {1}",  
    myGeoPoint.u_name, gr.getValue(distToLondon));
```

The output lists the distance between London and cities in the `u_location` field in meters.

```
Name: London  Dist to London(m): 0 
Name: Glasgow  Dist to London(m): 555985.58456358 
Name: Dublin  Dist to London(m): 464000.328892816 
Name: Miami  Dist to London(m): 7123803.25406323 
Name: Bermuda  Dist to London(m): 5547607.95564083 
Name: Puerto Rico  Dist to London(m): 6799201.00905107 
Name: Perth  Dist to London(m): 14485217.5596414 
Name: Sydney  Dist to London(m): 17001034.4875494 
Name: Tasmania  Dist to London(m): 17324634.4559516 
```

## Filter the distance between two geopoints

Use the `DISTANCE_SPHERE_WITHIN` query condition to filter for records having a geopoint value within the radius of a defined latitude, longitude point. 

`DISTANCE_SPHERE_WITHIN` must follow syntax `geopointDISTANCE_SPHERE_WITHINlongitude,latitude<radius` where:

-   `geopoint` is a geopoint field​
-   `longitude` and `latitude` are decimal constant​s
-   `radius` is a decimal constant \(in meters\)

**Note:** The less-than symbol \(&lt;\) in this expression is required and only used as a delimiter. Any other comparison operator is invalid.

The `DISTANCE_SPHERE_WITHIN` accepts kilometer or meter values in the request but always returns the output value in meters.

The following example script shows how to build an encoded query that returns only records having a `u_location` less than 1,000,000 kilometers away from the point `-0.189937` longitude, `51.473584` latitude \(which is roughly the location of London\). When executed, it returns three records representing cities within the specified radius of London.

```
const myGeoPoint = new GlideRecord("u_geopoint");  
myGeoPoint.addEncodedQuery("u_locationDISTANCE_SPHERE_WITHIN-0.189937,51.473584<1000000");  
myGeoPoint.query(); 
 
while(gr.next()) 
    gs.info("Name:" + myGeoPoint.getDisplayValue("u_name")   
         + " Location:" + myGeoPoint.getDisplayValue("u_location"));
```

Output:

```
Name:London Location:(-0.189937, 51.473584) 
Name:Dublin Location:(-6.304994, 53.348317) 
Name:Glasgow Location:(-4.223964, 55.867846)
```

The following example script is equivalent to the first but uses an alternative syntax for GlideRecord.

```
const myGeoPoint = new GlideRecord("u_geopoint");  
myGeoPoint.addQuery("u_location", "DISTANCE_SPHERE_WITHIN", "-0.189937,51.473584<1000000");  
myGeoPoint.query(); 
 
while(myGeoPoint.next()) 
    gs.info("Name:" + myGeoPoint.getDisplayValue("u_name")   
         + " Location:" + myGeoPoint.getDisplayValue("u_location"));
```

Output:

```
Name:London Location:(-0.189937, 51.473584) 
Name:Dublin Location:(-6.304994, 53.348317) 
Name:Glasgow Location:(-4.223964, 55.867846)
```

