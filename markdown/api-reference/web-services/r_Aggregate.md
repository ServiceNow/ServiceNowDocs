---
title: aggregate
description: Query a table using an aggregate function including SUM, COUNT, MIN, MAX, LAST, and AVG.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Retrieval, API functions, Direct services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# aggregate

Query a table using an aggregate function including SUM, COUNT, MIN, MAX, LAST, and AVG.

**Note:** Functionality described here requires the Aggregate Web Service plugin.

## Input fields

Any element of the target table. In addition, one or more of the aggregate functions \(SUM, COUNT, MIN, MAX, LAST, and AVG\).

A GROUP BY and a HAVING clause may also be added.

## Output fields

An aggregateResponse element encapsulating all field values for the record retrieved.

## Sample SOAP messages

Sample SOAP request using COUNT aggregate function.

```
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/encoding/"
                   xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/"
                   xmlns:m="http://www.service-now.com"
                   xmlns:tns="http://www.service-now.com/map"
                   xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                   xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                   SOAP-ENV:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/">
  <SOAP-ENV:Body>
    <aggregate>
      <COUNT>number</COUNT>
      <active>true</active>
    </aggregate>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

The resulting response of a COUNT aggregate function call looks like this:

```
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/"
                   xmlns:SOAP-ENC="http://schemas.xmlsoap.org/soap/encoding/" 
                   xmlns:m="http://www.service-now.com"
                   xmlns:tns="http://www.service-now.com/map"
                   xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                   xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                   SOAP-ENV:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/">
  <SOAP-ENV:Body>
    <aggregateResponse>
        <aggregateResult>
          <avg>2.7200</avg>
        </aggregateResult>
    </aggregateResponse>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

Sample SOAP request using AVG aggregate function with a GROUP BY clause.

```
<?xml version="1.0" encoding="UTF-8"?>
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENC="http://schemas.xmlsoap.org/soap/encoding/"
                   xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/"
                   xmlns:m="http://www.service-now.com"
                   xmlns:tns="http://www.service-now.com/map"
                   xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                   xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                   SOAP-ENV:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/">
  <SOAP-ENV:Body>
    <aggregate xmlns="http://www.service-now.com">
      <GROUP_BY>category</GROUP_BY>
      <active>true</active>
      <AVG>severity</AVG>
    </aggregate>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

The resulting response of a AVG aggregate function call with a GROUP BY clause looks like this:

```
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/"
                   xmlns:SOAP-ENC="http://schemas.xmlsoap.org/soap/encoding/"
                   xmlns:m="http://www.service-now.com"
                   xmlns:tns="http://www.service-now.com/map"
                   xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                   xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                   SOAP-ENV:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/">
  <SOAP-ENV:Body>
    <aggregateResponse>
        <aggregateResult>
          <avg>1.0000</avg>
          <category>database</category>
        </aggregateResult>
        <aggregateResult>
          <avg>3.0000</avg>
          <category>hardware</category>
        </aggregateResult>
        <aggregateResult>
          <avg>3.0000</avg>
          <category>inquiry</category>
        </aggregateResult>
        <aggregateResult>
          <avg>2.0000</avg>
          <category>network</category>
        </aggregateResult>
        <aggregateResult>
          <avg>2.6923</avg>
          <category>software</category>
        </aggregateResult>
    </aggregateResponse>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

Sample SOAP request using an encoded query to filter the aggregate:

```
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/encoding/"
                   xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/"
                   xmlns:m="http://www.service-now.com"
                   xmlns:tns="http://www.service-now.com/map"
                   xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                   xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                   SOAP-ENV:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/">
  <SOAP-ENV:Body>
    <aggregate>
      <COUNT>number</COUNT>
      <active>true</active>
      <__encoded_query>number=INC0000001^ORnumber=INC0000002</__encoded_query>
    </aggregate>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

Sample aggregate request using HAVING to narrow the results.

HAVING takes four fields. Each field is delimited by "^": the aggregate type, the field of the aggregate, the operation type, and the value to compare.

More than one HAVING can be added to the request, so you can use HAVING expressions, but there is no support for OR.

```
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/encoding/"
                   xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/"
                   xmlns:m="http://www.service-now.com"
                   xmlns:tns="http://www.service-now.com/map"
                   xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                   xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                   SOAP-ENV:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/">
  <SOAP-ENV:Body>
    <aggregate>
      <COUNT>sys_id</COUNT>
      <GROUP_BY>internal_type</GROUP_BY> 
      <HAVING>COUNT^*^>^10</HAVING>
      <HAVING>COUNT^*^<^20</HAVING>
      <COUNT>sys_id</COUNT>
      <active>true</active>
    </aggregate>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

**Parent Topic:**[Data Retrieval API](r_DataRetrievalAPI.md)

