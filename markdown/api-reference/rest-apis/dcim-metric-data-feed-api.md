---
title: DCIM Metric Data Feed API
description: The DCIM Metric Data Feed API provides an endpoint to accept Data Center Infrastructure Management \(DCIM\) metric data from an external system and store the data in a MetricBase database.Stores metric data such as temperature, humidity, and power usage into MetricBase.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# DCIM Metric Data Feed API

The DCIM Metric Data Feed API provides an endpoint to accept Data Center Infrastructure Management \(DCIM\) metric data from an external system and store the data in a MetricBase database.

This API receives near real-time metric data such as temperature, humidity, and power usage.

This API can be extended for use with a chosen external system by implementing the scripted extension point TNIDCIMFeedParser. The default implementation TNIDCIMFeedParserImpl can be used as an example. For more information about extension points, see [Using extension points to extend application functionality](../../../build/applications/concept/extension-points.md).

This API is included in the Network Inventory Advanced application, which is available on the ServiceNow Store. This API also requires the MetricBase plugin \(com.snc.clotho\).

The calling user must have the sn\_ni\_adv.metric\_integrator role.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## DCIM Metric Data Feed - POST /sn\_ni\_adv/dcim/feed/\{vendorname\}

Stores metric data such as temperature, humidity, and power usage into MetricBase.

By default, this endpoint can be used to store data about the following types of configuration items \(CIs\):

-   Circuit \[cmdb\_ci\_circuit\]
-   Cabinet \[cmdb\_ci\_container\_cabinet\]
-   Cage \[cmdb\_ci\_cage\]
-   Data Center \[cmdb\_ci\_datacenter\]
-   Data Center Zone \[cmdb\_ci\_zone\]

To use this endpoint with additional CI types, create metric definitions and implement the scripted extension point TNIDCIMFeedParser.

### URL format

Default URL: `/api/sn_ni_adv/dcim/feed/{vendorname}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

vendorname

</td><td>

Name of the external system to receive metric data from. When using the default implementation of this API, this value is `equinix`. When using this API with other external systems, the **vendorname** used here must be included in your implementation of the TNIDCIMFeedParser extension point.

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Required. The data to store in MetricBase. Data type: Object

**Note:** The elements that must included in this object vary based on the **type** parameter and the configuration item type, such as datacenter or circuit.

```
"data": {
   "apparentPower": {Object},
   "asset": {Object},
   "cabinet": "String",
   "cabinetRating": {Object},
   "cage": "String",
   "contractualPower": {Object},
   "ibx": "String",
   "kilowattHour": {Object},
   "peakLastSevenDays": {Object},
   "peakLastSevenDaysRatio": {Object},
   "powerConsumptionToContractual": {Object},
   "powerFactor": {Object},
   "reading": {Object},
   "readingTime": "String",
   "realPower": {Object},
   "soldCurrent": {Object},
   "tag": {Object}
}
```

</td></tr><tr><td>

data.apparentPower

</td><td>

Apparent power data in kilovolt-amperes. Required when the **type** parameter is `power`.Data type: Object

```
"apparentPower": {      
   "unit": "String",
   "value": "String"  
}
```

</td></tr><tr><td>

data.apparentPower.unit

</td><td>

Unit of measurement. The only accepted value is `kVA`.Data type: String

</td></tr><tr><td>

data.apparentPower.value

</td><td>

The recorded kilovolt-amperes reading.Data type: String

</td></tr><tr><td>

data.asset

</td><td>

Asset data. Required for circuits when the **type** parameter is `metered-power` or `power`. Required for cabinets, cages, and zones when the **type** parameter is `environmental`. Data type: Object

```
"asset": {
   "id": "String",
   "level": "String",
   "type": "String"
}
```

</td></tr><tr><td>

data.asset.id

</td><td>

Name of the asset.Table: Circuit \[cmdb\_ci\_circuit\], Cabinet \[cmdb\_ci\_container\_cabinet\], Cage \[cmdb\_ci\_cage\], or Data Center Zone \[cmdb\_ci\_zone\]

Field: Name

Data type: String

</td></tr><tr><td>

data.asset.level

</td><td>

Type of asset. Used for cabinets, cages, and zones.Possible values:

-   CABINET
-   CAGE
-   ZONE

Data type: String

</td></tr><tr><td>

data.asset.type

</td><td>

Type of asset. Used for circuits. The only accepted value is `CIRCUIT`.Data type: String

</td></tr><tr><td>

data.cabinet

</td><td>

Name of the cabinet. Required for cabinets when the **type** parameter is `metered-power` or `power`.Table: Container Cabinet \[cmdb\_ci\_container\_cabinet\]

Field: Name

Data type: String

</td></tr><tr><td>

data.cabinetRating

</td><td>

Power usage the cabinet is rated for in kilovolt-amperes. Required when the **type** parameter is `power`.Data type: Object

```
"cabinetRating": {      
   "unit": "String",
   "value": "String"  
}
```

</td></tr><tr><td>

data.cabinetRating.unit

</td><td>

Unit of measurement. The only accepted value is `kVA`.Data type: String

</td></tr><tr><td>

data.cabinetRating.value

</td><td>

The power usage rating for the cabinet.Data type: String

</td></tr><tr><td>

data.cage

</td><td>

Name of the cage. Required for cages when the **type** parameter is `metered-power` or `power`.Table: Cage \[cmdb\_ci\_cage\]

Field: Name

Data type: String

</td></tr><tr><td>

data.contractualPower

</td><td>

Power usage allotted by the contract in kilovolt-amperes. Required when the **type** parameter is `power`.Data type: Object

```
"contractualPower": {      
   "unit": "String",
   "value": "String"  
}
```

</td></tr><tr><td>

data.contractualPower.unit

</td><td>

Unit of measurement. The only accepted value is `kVA`.Data type: String

</td></tr><tr><td>

data.contractualPower.value

</td><td>

The power usage allotted by the contract.Data type: String

</td></tr><tr><td>

data.ibx

</td><td>

Name of the datacenter. Required when storing metric data for a datacenter.

Table: Data Center \[cmdb\_ci\_datacenter\]

Data type: String

</td></tr><tr><td>

data.kilowattHour

</td><td>

Power usage data in kilowatt-hours. Required when the **type** parameter is `metered-power`. Data type: Object

```
"kilowattHour": {      
   "unit": "String",
   "value": "String"  
}
```

</td></tr><tr><td>

data.kilowattHour.unit

</td><td>

Unit of measurement. The only accepted value is `kWh`.Data type: String

</td></tr><tr><td>

data.kilowattHour.value

</td><td>

The recorded kilowatt-hours reading.Data type: String

</td></tr><tr><td>

data.peakLastSevenDays

</td><td>

The maximum power usage within the last week in kilovolt-amperes. Required when the **type** parameter is `power`. Data type: Object

```
"peakLastSevenDays": {      
   "unit": "String",
   "value": "String"  
}
```

</td></tr><tr><td>

data.peakLastSevenDays.unit

</td><td>

Unit of measurement. The only accepted value is `kVA`.Data type: String

</td></tr><tr><td>

data.peakLastSevenDays.value

</td><td>

The maximum power usage value from the last week.Data type: String

</td></tr><tr><td>

data.peakLastSevenDaysRatio

</td><td>

The maximum percentage of power used out of the amount allotted by the contract within the last week. Required when the **type** parameter is `power`.Data type: Object

```
"peakLastSevenDaysRatio": {      
   "unit": "String",
   "value": "String"  
}
```

</td></tr><tr><td>

data.peakLastSevenDaysRatio.unit

</td><td>

Unit of measurement. The only accepted value is `PERCENT`.Data type: String

</td></tr><tr><td>

data.peakLastSevenDaysRatio.value

</td><td>

The maximum percent of power used.Data type: String

</td></tr><tr><td>

data.powerConsumptionToContractual

</td><td>

Percentage of power used out of the amount allotted by the contract. Required when the **type** parameter is `power`.Data type: Object

```
"powerConsumptionToContractual": {      
   "unit": "String",
   "value": "String"  
}
```

</td></tr><tr><td>

data.powerConsumptionToContractual.unit

</td><td>

Unit of measurement. The only accepted value is `PERCENT`.Data type: String

</td></tr><tr><td>

data.powerConsumptionToContractual.value

</td><td>

The percent of power used.Data type: String

</td></tr><tr><td>

data.powerFactor

</td><td>

Power factor data. Required when the **type** parameter is `power`.Data type: Object

```
"powerFactor": {      
   "unit": "String",
   "value": "String"  
}
```

</td></tr><tr><td>

data.powerFactor.unit

</td><td>

Unit of measurement. The only accepted value is `pf`.Data type: String

</td></tr><tr><td>

data.powerFactor.value

</td><td>

The power factor value.Data type: String

</td></tr><tr><td>

data.reading

</td><td>

The collected environmental data. Required when the **type** parameter is `environmental`. Data type: Object

```
"reading": {      
   "unit": "String",
   "value": "String"  
}
```

</td></tr><tr><td>

data.reading.unit

</td><td>

Unit of measurement.Possible values:

-   `CELSIUS`: Used when **data.tag.id** is `temperature`.
-   `PERCENT`: Used when **data.tag.id** is `humidity`.

Data type: String

</td></tr><tr><td>

data.reading.value

</td><td>

The recorded value.Data type: String

</td></tr><tr><td>

data.readingTime

</td><td>

Required. Date and time the data was collected. This value must be in UTC in ISO 8601 format. For example, `2025-07-03T16:22:15.000Z`.

Data type: String

</td></tr><tr><td>

data.realPower

</td><td>

Power usage data in kilowatts. Required when the **type** parameter is `power`. Data type: Object

```
"realPower": {      
   "unit": "String",
   "value": "String"  
}
```

</td></tr><tr><td>

data.realPower.unit

</td><td>

Unit of measurement. The only accepted value is `kW`.Data type: String

</td></tr><tr><td>

data.realPower.value

</td><td>

The recorded kilowatts reading.Data type: String

</td></tr><tr><td>

data.soldCurrent

</td><td>

Electric current allotted by the contract in amps. Required when the **type** parameter is `power`.Data type: Object

```
"soldCurrent": {      
   "unit": "String",
   "value": "String"  
}
```

</td></tr><tr><td>

data.soldCurrent.unit

</td><td>

Unit of measurement. The only accepted value is `A`.Data type: String

</td></tr><tr><td>

data.soldCurrent.value

</td><td>

The electric current allotted by the contract.Data type: String

</td></tr><tr><td>

data.tag

</td><td>

Object containing the type of environmental data. Required when the **type** parameter is `environmental`.Data type: Object

```
"tag": {
   "id": "String"
}
```

</td></tr><tr><td>

data.tag.id

</td><td>

The type of environmental data.Possible values:

-   humidity
-   temperature

Data type: String

</td></tr><tr><td>

type

</td><td>

Required. Type of metric data.Possible values:

-   `environmental`: Used for humidity or temperature.
-   `metered-power`: Used for power usage in kilowatt-hours \(kWh\).
-   `power`: Used for power usage in kilowatts \(kW\) and kilovolt-amperes \(kVA\).

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json;charset=UTF-8**.|
|Authorization|Basic.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json;charset=UTF-8**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|429|Too many requests.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details about the request.Data type: Object

```
"result": {
   "status": "String",
   "sys_id": "String"
}
```

</td></tr><tr><td>

result.status

</td><td>

Status of the request.Data type: String

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the CI updated with the metric data.Table: Circuit \[cmdb\_ci\_circuit\], Cabinet \[cmdb\_ci\_container\_cabinet\], Cage \[cmdb\_ci\_cage\], Data Center \[cmdb\_ci\_datacenter\], or Data Center Zone \[cmdb\_ci\_zone\]

Data type: String

</td></tr></tbody>
</table>### cURL request

Stores metered power data for a datacenter.

```
curl "https://instance.service-now.com/api/sn_ni_adv/dcim/feed/vendorname" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    "type": "metered-power",
    "data": {
        "ibx": "Datacenter Name",
        "kilowattHour": {
            "value": "40509.323",
            "unit": "kWh"
        },
        "readingTime": "2025-07-03T16:22:15.000Z"
    }
}" \
--user 'username':'password'
```

Response body.

```
{
    "result": {
        "status": "success",
        "sys_id": "c88dde85ff2662109cb9ffffffffffcc"
    }
}
```

### cURL request

Stores power data for a circuit.

```
curl "https://instance.service-now.com/api/sn_ni_adv/dcim/feed/vendorname" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    "type": "power",
    "data": {
        "asset": {
            "id": "Circuit Name",
            "type": "CIRCUIT"
        },
        "realPower": {
            "value": "0.522",
            "unit": "kW"
        },
        "apparentPower": {
            "value": "1.070",
            "unit": "kVA"
        },
        "contractualPower": {
            "value": "60.000",
            "unit": "kVA"
        },
        "powerFactor": {
            "value": "0.48",
            "unit": "pf"
        },
        "soldCurrent": {
            "value": "15.000",
            "unit": "A"
        },
        "powerConsumptionToContractual": {
            "value": "32.151",
            "unit": "PERCENT"
        },
        "cabinetRating": {
            "value": "123.300",
            "unit": "kVA"
        },
        "peakLastSevenDays": {
            "value": "1.146",
            "unit": "kVA"
        },
        "peakLastSevenDaysRatio": {
            "value": "34.424",
            "unit": "PERCENT"
        },
        "readingTime": "2025-07-03T16:22:15.000Z"
    }
}" \
--user 'username':'password'
```

Response body.

```
{
    "result": {
        "status": "success",
        "sys_id": "c67dbe45fc2662109cb9ffffffffffcd"
    }
}
```

### cURL request

Stores temperature data for a zone.

```
curl "https://instance.service-now.com/api/sn_ni_adv/dcim/feed/vendorname" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    "type": "environmental",
    "data": {
        "asset": {
            "id": "Zone Name",
            "level": "ZONE"
        },
        "reading": {
            "value": "23.300",
            "unit": "CELSIUS"
        },
        "tag": {
            "id": "temperature"
        },
        "readingTime": "2025-07-03T16:22:15.000Z"
    }
}" \
--user 'username':'password'
```

Response body.

```
{
    "result": {
        "status": "success",
        "sys_id": "c64dbc42fe2862109cb9ffffffffffed"
    }
}
```

### cURL request

Stores humidity data for a cabinet.

```
curl "https://instance.service-now.com/api/sn_ni_adv/dcim/feed/vendorname" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    "type": "environmental",
    "data": {
        "asset": {
            "id": "Test Cabinet",
            "level": "CABINET"
        },
        "reading": {
            "value": "66.120",
            "unit": "PERCENT"
        },
        "tag": {
            "id": "humidity"
        },
        "readingTime": "2025-07-03T16:22:15.000Z"
    }
}" \
--user 'username':'password'
```

Response body.

```
{
    "result": {
        "status": "success",
        "sys_id": "c24dbc82fe3862107cb9ffffffffffbc"
    }
}
```

