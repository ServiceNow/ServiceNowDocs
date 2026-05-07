---
title: Prisma Cloud REST Messages
description: Prisma REST messages are used to make calls to the Prisma Application Programming Interface \(API\) to fetch the compliance data.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Understanding the Vulnerability Response Integration with Palo Alto Prisma Cloud, Integrate with other applications, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Prisma Cloud REST Messages

Prisma REST messages are used to make calls to the Prisma Application Programming Interface \(API\) to fetch the compliance data.

The following REST messages are shipped with the base system.

## Prisma Cloud integrations

All Prisma Cloud integrations use the JSON Web Token \(JWT\) for authentication and authorization.

<table id="table_v2g_x1q_dt"><thead><tr><th>

Endpoint

</th><th>

Description

</th><th>

Method

</th><th>

Body

</th><th>

API documentation link

</th></tr></thead><tbody><tr><td>

/login

</td><td>

Obtains the JWT token for use in all subsequent integrations.

</td><td>

POST

</td><td>

```
{ "username": <<access key id >>, 
"password": <<secret access key>>}
```

</td><td>

[https://pan.dev/prisma-cloud/api/cspm/app-login/](https://pan.dev/prisma-cloud/api/cspm/app-login/)

</td></tr></tbody>
</table>|Endpoint|Description|Method|Body|API documentation link|
|--------|-----------|------|----|----------------------|
|/auth\_token/extend|Automatically renews the JWT token on expiration. The default duration for token expiry is 60 minutes.|GET|NA|[https://pan.dev/prisma-cloud/api/cspm/extend-session/](https://pan.dev/prisma-cloud/api/cspm/extend-session/)|

|Endpoint|Description|Method|Body|API documentation link|
|--------|-----------|------|----|----------------------|
|/v2/policy|Retrieves all the policy data from Prisma.|GET|NA|[https://pan.dev/prisma-cloud/api/cspm/get-policies/](https://pan.dev/prisma-cloud/api/cspm/get-policies/)|

<table id="table_tjw_nrf_t1c"><thead><tr><th>

Endpoint

</th><th>

Description

</th><th>

Method

</th><th>

Body

</th><th>

API documentation link

</th></tr></thead><tbody><tr><td>

/v2/alert

</td><td>

Retrieves all alerts from Prisma.

</td><td>

POST

</td><td>

```
{
    "detailed": "false",
    "filters": [
	{

		"name": "timeRange.type",
                "operator": "=",
                "value": "ALERT_STATUS_UPDATED"
        }
    ],
    "sortBy": [
        "resource.id"
    ],
    "pageToken": "",
    "offset": 0,
    "limit": 2000,
    "timeRange": {
        "type": "absolute",
        "value": {
            "startTime": <<Import since at integration level>>,
            "endTime": << Current integration  run time>>
        }
    }
}
```

</td><td>

[https://pan.dev/prisma-cloud/api/cspm/post-alerts/](https://pan.dev/prisma-cloud/api/cspm/post-alerts/)

</td></tr></tbody>
</table>For Prisma Comprehensive Alert integration, the filters in the above POST body must be replaced as follows:

```
"filters": [
	{
                    "name": "alert.status",
                    "operator": "=",
                    "value": "open"
                },
                {
                    "name": "alert.status",
                    "operator": "=",
                    "value": "dismissed"
                },
                {
                    "name": "alert.status",
                    "operator": "=",
                    "value": "snoozed"
                },
                {
                    "name": "alert.status",
                    "operator": "=",
                    "value": "pending_resolution"
                },
                {
                    "name": "timeRange.type",
                    "operator": "=",
                    "value": "ALERT_UPDATED"
                }
 
    ],
```

