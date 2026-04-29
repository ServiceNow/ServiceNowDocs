---
title: NLU system entities
description: Use globally defined NLU entities to identify system information that Virtual Agent can extract from the conversation. You can define entities as "nodeless" input variables for a topic. These variables can be slot-filled from NLU service provider predictions or provided outside of the scope of the topic.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Virtual Agent technical reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# NLU system entities

Use globally defined NLU entities to identify system information that Virtual Agent can extract from the conversation. You can define entities as "nodeless" input variables for a topic. These variables can be slot-filled from NLU service provider predictions or provided outside of the scope of the topic.

System entities are enabled in NLU models by default. You can view them on the model **Entities** tab in NLU Workbench.

## GLOBAL.DATE system entity

The DAY SubType returns a date string that is accurate to a specific date.

<table id="table_lcl_cjd_lpb"><thead><tr><th>

Usage

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Format

</td><td>

YYYY-MM-DD

</td></tr><tr><td>

Regular expression

</td><td>

\\\\d\\\\d\\\\d\\\\d-\\\\d\\\\d-\\\\d\\\\d

</td></tr><tr><td>

Input example

</td><td>

Mr. Smith left Friday, February 4, 2019.

</td></tr><tr><td>

Normalized value

</td><td>

2019-02-04

</td></tr><tr><td>

Code example

</td><td>

```
{
"name": "DATE", 
"value": "...",
"score": 1.0, 
"normalization": "2019-02-04"
}

```

</td></tr></tbody>
</table>The WEEK SubType returns a date string of a specific week of a year.

<table id="table_crg_tjd_lpb"><thead><tr><th>

Usage

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Format

</td><td>

YYYY'W'WW

</td></tr><tr><td>

Regular expression

</td><td>

\\\\d\\\\d\\\\d\\\\d\\\\dW\\\\d\\\\d

</td></tr><tr><td>

Input example

</td><td>

Mr. Smith left the third week of 1999.

</td></tr><tr><td>

Normalized value

</td><td>

1999W3

</td></tr><tr><td>

Code example

</td><td>

```
{
"name": "entity:GLOBAL.DATE", 
"value": "...",
"score": 1.0, 
"normalization": {"type": "GLOBAL.DATE", "subType": "WEEK", "value":"1999W3"}
}

```

</td></tr></tbody>
</table>The MONTH SubType returns a date string of a specific month of a year.

<table id="table_edh_sld_lpb"><thead><tr><th>

Usage

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Format

</td><td>

YYYY'M'MM

</td></tr><tr><td>

Regular expression

</td><td>

\\\\d\\\\d\\\\d\\\\dM\\\\d\\\\d

</td></tr><tr><td>

Input example

</td><td>

Mr. Smith left in February of 1999.

</td></tr><tr><td>

Normalized value

</td><td>

1999M02

</td></tr><tr><td>

Code example

</td><td>

```
{
"name": "entity:GLOBAL.DATE",
"value": "...",
"score": 1.0, 
"normalization": {"type": "GLOBAL.DATE", "subType": "MONTH", "value": "1999M02"}
}

```

</td></tr></tbody>
</table>The YEAR SubType returns a date string of a specific year.

<table id="table_pxj_1md_lpb"><thead><tr><th>

Usage

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Format

</td><td>

YYYY

</td></tr><tr><td>

Regular expression

</td><td>

\\\\d\\\\d\\\\d\\\\d

</td></tr><tr><td>

Input example

</td><td>

Mr. Smith left in 1999.

</td></tr><tr><td>

Normalized value

</td><td>

1999

</td></tr><tr><td>

Code example

</td><td>

```
{
"name": "entity:GLOBAL.DATE",
"value": "...",
"score": 1.0,
"normalization": {"type": "GLOBAL.DATE", "subType": "YEAR", "value": "1999"}
}

```

</td></tr></tbody>
</table>The SEASON SubType returns a date string of a specific season of the year.

<table id="table_s1q_fpd_lpb"><thead><tr><th>

Usage

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Format

</td><td>

One of the following:-   **Winter**: YYYYWI
-   **Spring**: YYYYSP
-   **Summer**: YYYYSU
-   **Fall**: YYYYFA

</td></tr><tr><td>

Regular expression

</td><td>

One of the following:-   **Winter**: \\\\d\\\\d\\\\d\\\\dWI
-   **Spring**: \\\\d\\\\d\\\\d\\\\dSP
-   **Summer**: \\\\d\\\\d\\\\d\\\\dSU
-   **Fall**: \\\\d\\\\d\\\\d\\\\dFA

</td></tr><tr><td>

Input example

</td><td>

Mr. Smith left in the fall of 1999.

</td></tr><tr><td>

Normalized value

</td><td>

1999FA

</td></tr><tr><td>

Code example

</td><td>

```
{
"name": "entity:GLOBAL.DATE",
"value": "...",
"score": 1.0,
"normalization": {"type": "GLOBAL.DATE", "subType": "SEASON", "value": "1999FA"}
}

```

</td></tr></tbody>
</table>## GLOBAL.TIME system entity

The TIME SubType returns a time string that is accurate to an hour and a minute.

<table id="table_zrm_mqd_lpb"><thead><tr><th>

Usage

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Format

</td><td>

'T'HH:mm

</td></tr><tr><td>

Regular expression

</td><td>

T\\\\d\\\\d:\\\\d\\\\d

</td></tr><tr><td>

Input example

</td><td>

Mr. Smith left at ten minutes to three.

</td></tr><tr><td>

Normalized value

</td><td>

T02:50

</td></tr><tr><td>

Code example

</td><td>

```
{
"name": "entity:GLOBAL.TIME", 
"value": "...",
"score": 1.0, 
"normalization": {"type": "GLOBAL.TIME","subType": "TIME", "value": "T02:50"}
}

```

</td></tr></tbody>
</table>The PARTSOFDAY SubType returns a time string that specifies parts of the day.

<table id="table_thr_wqd_lpb"><thead><tr><th>

Usage

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Format

</td><td>

One of the following:-   **Morning**: TMO
-   **Afternoon**: TAF
-   **Evening**: TEV
-   **Night**: TNI

</td></tr><tr><td>

Regular expression

</td><td>

One of the following:-   **Morning**: TMO
-   **Afternoon**: TAF
-   **Evening**: TEV
-   **Night**: TNI

</td></tr><tr><td>

Input example

</td><td>

Mr. Smith left in the morning.

</td></tr><tr><td>

Normalized value

</td><td>

TMO

</td></tr><tr><td>

Code example

</td><td>

```
{
"name": "entity:GLOBAL.TIME", 
"value": "...",
"score": 1.0, 
"normalization": {"type": "GLOBAL.TIME", "subType": "PARTSOFDAY", "value": "TMO"}
}

```

</td></tr></tbody>
</table>## GLOBAL.DATE\_TIME system entity

The DATE\_TIME SubType returns a date string that is accurate to a specific date and time string that is accurate to an hour and a minute.

<table id="table_wsh_ybc_3vb"><thead><tr><th>

Usage

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Format

</td><td>

YYYY-MM-DD'T'HH:mm

</td></tr><tr><td>

Regular expression

</td><td>

\\\\d\\\\d\\\\d\\\\d-\\\\d\\\\d-\\\\d\\\\dT\\\\d\\\\d:\\\\d\\\\d

</td></tr><tr><td>

Input example

</td><td>

Mr. Smith leaves on October 31st at 5:00 p.m.

</td></tr><tr><td>

Normalized value

</td><td>

2022-10-31T17:00

</td></tr><tr><td>

Code example

</td><td>

```
{
"name": "DATE_TIME",
"value": "October 31st at 5:00 p.m",
"normalization": "2022-10-31T17:00","confidence": "1"
}
```

</td></tr></tbody>
</table>## GLOBAL.DURATION system entity

This entity returns a duration string that specifies the duration of the activity.

<table id="table_gf3_mrd_lpb"><thead><tr><th>

Usage

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Format

</td><td>

One of the following:-   **Second**: 's'ss
-   **Minute**: 'm'mm
-   **Hour**: 'h'hh
-   **Day**: 'D'DD
-   **Week**: 'W'WW
-   **Month**: 'M'MM
-   **Year**: 'Y'YY

</td></tr><tr><td>

Regular expression

</td><td>

One of the following:-   **Second**: s\\\\d\\\\d
-   **Minute**: m\\\\d\\\\d
-   **Hour**: h\\\\d\\\\d
-   **Day**: D\\\\d\\\\d
-   **Week**: W\\\\d\\\\d
-   **Month**: M\\\\d\\\\d
-   **Year**: Y\\\\d\\\\d

</td></tr><tr><td>

Input example

</td><td>

Mr. Smith stayed in Boston for 48 hours.

</td></tr><tr><td>

Normalized value

</td><td>

h48

</td></tr><tr><td>

Code example

</td><td>

```
{
"name": "entity:GLOBAL.DURATION",
"value": "...", 
"score": 1.0,
"normalization": {"type": "GLOBAL.DURATION", "value": "h48"}
}

```

</td></tr></tbody>
</table>## GLOBAL.LOCATION system entity

This entity returns a location string.

<table id="table_wd5_cvd_lpb"><thead><tr><th>

Usage

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Format

</td><td>

String value. Example: `Santa Clara`

</td></tr><tr><td>

Regular expression

</td><td>

Not applicable.

</td></tr><tr><td>

Input example

</td><td>

Mr. Smith works in Santa Clara.

</td></tr><tr><td>

Normalized value

</td><td>

Santa Clara

</td></tr><tr><td>

Code example

</td><td>

```
{
"name": "entity:GLOBAL.LOCATION",
"value": "...", 
"score": 1.0,
"normalization": {"type": "GLOBAL.LOCATION", "value":"Santa Clara"}
}

```

</td></tr></tbody>
</table>## GLOBAL.PERSON system entity

This entity returns a name string.

<table id="table_og1_nvd_lpb"><thead><tr><th>

Usage

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Format

</td><td>

String value. Example: `Joe Smith`

</td></tr><tr><td>

Regular expression

</td><td>

Not applicable.

</td></tr><tr><td>

Input example

</td><td>

Joe Smith works in Santa Clara.

</td></tr><tr><td>

Normalized value

</td><td>

Joe Smith

</td></tr><tr><td>

Code example

</td><td>

```
{
"name": "entity:GLOBAL.PERSON", 
"value": "...",
"score": 1.0, 
"normalization": {"type": "GLOBAL.PERSON", "value":"Joe Smith"}
}

```

</td></tr></tbody>
</table>## GLOBAL.MONEY system entity

This entity returns a currency string.

<table id="table_c1b_wvd_lpb"><thead><tr><th>

Usage

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Format

</td><td>

String value. Example: `USD 2000`

</td></tr><tr><td>

Regular expression

</td><td>

Not applicable.

</td></tr><tr><td>

Input example

</td><td>

Show me laptops for less than $2000.

</td></tr><tr><td>

Normalized value

</td><td>

USD 2000**Note:** The normalized value uses the three-letter ISO 3166 country code of the source currency.

</td></tr><tr><td>

Code example

</td><td>

```
{
"name": "entity:GLOBAL.MONEY", 
"value": "...",
"score": 1.0, 
"normalization": {"type": "GLOBAL.MONEY", "value":"2000", “currency”:”USD”}
}

```

</td></tr></tbody>
</table>## GLOBAL.NUMBER system entity

This entity returns a number.

<table id="table_jxp_byd_lpb"><thead><tr><th>

Usage

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Format

</td><td>

String value. Example: `5.0`

</td></tr><tr><td>

Regular expression

</td><td>

Not applicable.

</td></tr><tr><td>

Input example

</td><td>

I want to see the previous 5 transactions from my account.

</td></tr><tr><td>

Normalized value

</td><td>

5.0

</td></tr><tr><td>

Code example

</td><td>

```
{
"name": "entity:GLOBAL.NUMBER",
  "value": "...",
  "score": 1.0,
  "normalization": {"numericValue":"5", “normalizedValue”: “5”}
}

```

</td></tr></tbody>
</table>## GLOBAL.SOFTWARE

Returns a software string.

<table id="table_oq4_vcy_brb"><thead><tr><th>

Usage

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Format

</td><td>

String value. Example: `Java`

</td></tr><tr><td>

Regular expression

</td><td>

Not applicable.

</td></tr><tr><td>

Input example

</td><td>

How do I install Java?

</td></tr><tr><td>

Normalized value

</td><td>

Java

</td></tr><tr><td>

Code example

</td><td>

```
{
  "name": "entity:GLOBAL.SOFTWARE",
  "value": "Java",
  "score": 0.99930537,
  "normalization": {"type":"entity:GLOBAL.SOFTWARE",
                     "subType":"SOFTWARE",
                     "value":"Java"}
}

```

</td></tr></tbody>
</table>## GLOBAL.HARDWARE

Returns a hardware string.

<table id="table_dfl_ycy_brb"><thead><tr><th>

Usage

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Format

</td><td>

String value. Example: `printer`

</td></tr><tr><td>

Regular expression

</td><td>

Not applicable.

</td></tr><tr><td>

Input example

</td><td>

How do I order a printer?

</td></tr><tr><td>

Normalized value

</td><td>

printer

</td></tr><tr><td>

Code example

</td><td>

```
{
  "name": "entity:GLOBAL.HARDWARE",
  "value": "printer",
  "score": 1.0,
  "normalization": {"type":"entity:GLOBAL.HARDWARE",
                     "subType":"HARDWARE",
                     "value":"printer"}
}

```

</td></tr></tbody>
</table>## Example NLU prediction result using Software system entity

```
{"status":"success",
   "response":{
      "utterance":"How do I install Java?",
      "intents":[
         {
            "intentName":"test intent",
            "nluModelName":"ml_x_snc_global_global_268a97a9dbd23c107906265d1396191a",
            "score":0.90401393,
            "intents":[
               
            ],
            "entities":[
               {
                  "name":"entity:GLOBAL.SOFTWARE",
                  "value":"Java",
                  "score":0.99930537,
                  "normalization":{
                     "type":"entity:GLOBAL.SOFTWARE",
                     "subType":"SOFTWARE",
                     "value":"Java"
                  },
                  "startingPosition":-1
               }
            ]
         }
      ],
      "properties":{
         "all:ml_x_snc_global_global_268a97a9dbd23c107906265d1396191a":"0.55",
         "entity:all":"0.01",
         "inference.sspace.time":"4",
         "inference.time":"33",
         "intent:all":"0.01",
         "nluPlatformLanguage":"en",
         "nluPlatformVersion":"rome.0"
      }
   }
}

```

## Example NLU prediction result using DATE system entity

```
{
    "utterance": "We should meet next Sunday at Starbucks.",
    "intents": [
        {
            "intentName": "intent:Desire.Desire",
            "score": 0.83452,
            "entities": []
        },
        {
            "intentName": "intent:Meeting.MeetRequest",
            "score": 0.8919042,
            "entities": [
                {
                    "entityName": "entity:Meeting.MeetRequest.Where",
                    "value": "Starbucks",
                    "score": 1
                },
     {
                    "entityName": "entity:GLOBAL.DATE",
                    "value": "Sunday",
                    "normalization": { "type": "DATE",
                        "subType": "DAY",
                        "value": "1999-10-01"
                     },
                    "score": 0.87
                }
            ]
        }
    ]
}

```

**Parent Topic:**[Virtual Agent technical reference](../concept/va-advanced-technical-reference.md)

**Related topics**  


[Domain separation and Virtual Agent](../concept/domain-separation-virtual-agent.md)

[Virtual Agent interaction records](../concept/va-interactions.md)

[Virtual Agent scripts](../concept/virtual-agent-scripts.md)

[Input data types in Virtual Agent topics](va-data-types.md)

[Virtual Agent URL parameters](va-sysparm.md)

[Latency feedback in Virtual Agent](latency-feedback.md)

