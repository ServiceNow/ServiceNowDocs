---
title: Performance Analytics API examples
description: These examples demonstrate how to perform a REST query using cURL commands, and show the data returned for each command. Each example builds upon the last, with later examples using the data returned by earlier examples.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 15
breadcrumb: [Integrate Performance Analytics, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Performance Analytics API examples

These examples demonstrate how to perform a REST query using cURL commands, and show the data returned for each command. Each example builds upon the last, with later examples using the data returned by earlier examples.

## Return all indicators that are displayed in the Analytics Hub

You can request a list of all indicators that are displayed in the Analytics Hub, including their unique record identifiers.

**Note:** These examples use the macOS syntax for curl commands. The Windows syntax can differ.

Command:

```
curl -v -u "user:password" -H "Accept:application/json" "https://instance.service-now.com/api/now/v1/pa/scorecards"
```

The following response is truncated to show only the Number of open incidents indicator, which is used in the other examples on this page:

```
//{
  "result" : [
...
  
    {
      "change_formatted" : "",
      "key" : false,
      "value_unit" : "",
      "value_formatted" : "",
      "period_title" : null,
      "gapperc" : null,
      "gap" : null,
      "target" : null,
      "period" : null,
      "target_formatted" : "",
      "favorite" : false,
      "direction_label" : "Minimize",
      "uuid" : "fb007202d7130100b96d45a3ce6103b4",
      "name" : "Number of open incidents",
      "value_color" : "#000000",
      "frequency_label" : "Daily",
      "change" : null,
      "gap_formatted" : "",
      "gapperc_formatted" : "",
      "value" : null,
      "unit" : {
        "display_value" : "#",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value" : "17b365e2d7320100ba986f14ce6103ad"
      },
      "changeperc_formatted" : "",
      "direction" : 2,
      "frequency" : 10,
      "precision" : 0,
      "changeperc" : null,
      "indicator" : {
        "display_value" : "Number of open incidents",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value" : "fb007202d7130100b96d45a3ce6103b4"
      },
      "description" : "Number of incidents open based on resolved date is empty."
    },
...
    
  ]
}
```

## Return indicator details

You can query the Analytics Hub for a particular indicator by providing the **sysparm\_uuid** parameter with an indicator sys\_id value. In this case, you use the sys ID for the Number of open incidents indicator, which you retrieved in the first example, when you got all the indicators in the Analytics Hub:

```
"uuid" : "fb007202d7130100b96d45a3ce6103b4",
"name" : "Number of open incidents",
```

Command:

```
curl -v -u "user:password" -H "Accept:application/json" "https://instance.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4"
```

Response:

```
{
  "result" : [
    {
      "change_formatted" : "",
      "key" : false,
      "value_unit" : "",
      "value_formatted" : "",
      "period_title" : null,
      "gapperc" : null,
      "gap" : null,
      "target" : null,
      "period" : null,
      "target_formatted" : "",
      "favorite" : false,
      "direction_label" : "Minimize",
      "uuid" : "fb007202d7130100b96d45a3ce6103b4",
      "name" : "Number of open incidents",
      "value_color" : "#000000",
      "frequency_label" : "Daily",
      "change" : null,
      "gap_formatted" : "",
      "gapperc_formatted" : "",
      "value" : null,
      "unit" : {
        "display_value" : "#",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value" : "17b365e2d7320100ba986f14ce6103ad"
      },
      "changeperc_formatted" : "",
      "direction" : 2,
      "frequency" : 10,
      "precision" : 0,
      "changeperc" : null,
      "indicator" : {
        "display_value" : "Number of open incidents",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value" : "fb007202d7130100b96d45a3ce6103b4"
      },
      "description" : "Number of incidents open based on resolved date is empty."
    }
  ]
}
```

## Return all breakdowns and aggregates for an indicator

You can query a list of available breakdowns and aggregates for an indicator by setting the **sysparm\_include\_available\_breakdowns** and **sysparm\_include\_available\_aggregates** parameters to true.

Command:

```
curl -v -u "user:password" -H "Accept:application/json" "https://instance.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4&sysparm_include_available_breakdowns=true&sysparm_include_available_aggregates=true"
```

Response:

```
{
  "result" : [
    {
      "key" : false,
      "change_formatted" : "",
      "aggregates" : [
        {
          "display_value" : "7d running SUM",
          "link" : "https://instance.service-now.com/api/now/v1/table/pa_aggregates/89ea4c11d7001100ba986f14ce6103dc",
          "value" : "89ea4c11d7001100ba986f14ce6103dc"
        },
        {
          "display_value" : "28d running SUM",
          "link" : "https://instance.service-now.com/api/now/v1/table/pa_aggregates/4dfa4c11d7001100ba986f14ce6103e2",
          "value" : "4dfa4c11d7001100ba986f14ce6103e2"
        },
        {
          "display_value" : "30d running SUM",
          "link" : "https://instance.service-now.com/api/now/v1/table/pa_aggregates/3e409011d7001100ba986f14ce610319",
          "value" : "3e409011d7001100ba986f14ce610319"
        },
        // Aggregates truncated for brevity
        
      ],
      "changeperc" : null,
      "value_formatted" : "",
      "period_title" : null,
      "gapperc" : null,
      "value_unit" : "",
      "target" : null,
      "period" : null,
      "target_formatted" : "",
      "favorite" : false,
      "gap" : null,
      "direction_label" : "Minimize",
      "uuid" : "fb007202d7130100b96d45a3ce6103b4",
      "name" : "Number of open incidents",
      "value_color" : "#000000",
      "frequency_label" : "Daily",
      "change" : null,
      "gap_formatted" : "",
      "gapperc_formatted" : "",
      "value" : null,
      "unit" : {
        "display_value" : "#",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value" : "17b365e2d7320100ba986f14ce6103ad"
      },
      "breakdowns" : [
        {
          "display_value" : "Priority",
          "link" : "https://instance.service-now.com/api/now/v1/table/pa_breakdowns/0df47e02d7130100b96d45a3ce610399",
          "value" : "0df47e02d7130100b96d45a3ce610399"
        },
        {
          "display_value" : "Category",
          "link" : "https://instance.service-now.com/api/now/v1/table/pa_breakdowns/1f918835d7231100b96d45a3ce6103fe",
          "value" : "1f918835d7231100b96d45a3ce6103fe"
        },
        {
          "display_value" : "Assignment Group",
          "link" : "https://instance.service-now.com/api/now/v1/table/pa_breakdowns/baec0752bf130100b96dac808c0739ed",
          "value" : "baec0752bf130100b96dac808c0739ed"
        },
        // Information for State and Age indicators truncated
        
      ],
      "changeperc_formatted" : "",
      "frequency" : 10,
      "precision" : 0,
      "direction" : 2,
      "indicator" : {
        "display_value" : "Number of open incidents",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value" : "fb007202d7130100b96d45a3ce6103b4"
      },
      "description" : "Number of incidents open based on resolved date is empty."
    }
  ]
}
```

## Return a time series aggregation of indicator scores

You can apply the 7d running SUM aggregate to the Analytics Hub using the **sysparm\_uuid** value with the sys\_id of the aggregate.

Command:

```
curl -v -u "user:password" -H "Accept:application/json" "https://instance.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4:89ea4c11d7001100ba986f14ce6103dc"
```

Response:

```
{
  "result" : [
    {
      "key" : false,
      "change_formatted" : "",
      "value_unit" : "",
      "value_formatted" : "",
      "period_title" : null,
      "aggregate" : {
        "display_value" : "7d running SUM",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_aggregates/89ea4c11d7001100ba986f14ce6103dc",
        "value" : "89ea4c11d7001100ba986f14ce6103dc"
      },
      "gapperc" : null,
      "target" : null,
      "period" : null,
      "target_formatted" : "",
      "favorite" : false,
      "gap" : null,
      "direction_label" : "Minimize",
      "uuid" : "fb007202d7130100b96d45a3ce6103b4:89ea4c11d7001100ba986f14ce6103dc",
      "name" : "Number of open incidents / 7d running SUM",
      "value_color" : "#000000",
      "frequency_label" : "Daily",
      "change" : null,
      "gap_formatted" : "",
      "gapperc_formatted" : "",
      "value" : null,
      "unit" : {
        "display_value" : "#",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value" : "17b365e2d7320100ba986f14ce6103ad"
      },
      "changeperc_formatted" : "",
      "direction" : 2,
      "frequency" : 10,
      "precision" : 0,
      "changeperc" : null,
      "indicator" : {
        "display_value" : "Number of open incidents",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value" : "fb007202d7130100b96d45a3ce6103b4"
      },
      "description" : "Number of incidents open based on resolved date is empty."
    }
  ]
}
```

## Return the elements for a breakdown

To get the scores associated with each element of a breakdown, and to get the sys\_ids of those elements, use the **sysparm\_breakdown** parameter with the sys\_id of the breakdown. In this example, you get the elements of the Assignment Group breakdown for the Number of open incidents indicator. From previous example, you have the sys\_id of `fb007202d7130100b96d45a3ce6103b4` for the Number of open incidents indicator and the sys\_id of `baec0752bf130100b96dac808c0739ed` for the Assignment Group breakdown.

Command:

```
curl -v -u "user:password" -H "Accept:application/json" "https://<instance>.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4&sysparm_breakdown=baec0752bf130100b96dac808c0739ed"
```

The response consists of a set of `indicator` objects, each containing one `element` object. The `element` objects each contain the name and sys\_id of an object. Because the information about the indicator is the same for each `indicator` object, in this example only the first `indicator` object is given in detail.

Response:

```
{
  "result":[
    { 
      "indicator": {
        "display_value":"Number of open incidents",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value":"fb007202d7130100b96d45a3ce6103b4"
      },
      "gap_formatted":"",
      "benchmarking":false,
      "frequency_label":"Daily",
      "changeperc_formatted":"0.0%",
      "direction_label":"Minimize",
      "precision":0,
      "breakdown": {
        "display_value":"Assignment Group",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_breakdowns/baec0752bf130100b96dac808c0739ed",
        "value":"baec0752bf130100b96dac808c0739ed"
      },
      "personal_target":null,
      "description":"Number of incidents open based on resolved date is empty.",
      "value_color":"#455464",
      "uuid":"fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:unmatched",
      "frequency":10,
      "gap":null,
      "value_unit":"14",
      "indicator_frequency":10,
      "value":14.0,
      "indicator_aggregate":1,
      "facts_table": {
        "name":"incident",
        "label":"Incidents"
      },
      "key":false,
      "indicator_frequency_label":"Daily",
      "direction":2,
      "element": {
        "display_value":"Unassigned",      //Element name
        "link":"https://<instance>.service-now.com/api/now/v1/table/sys_user_group/unmatched",
        "value":"unmatched"                //No sys_id for unmatched scores
      },
      "period_title":"Jul 22",
      "period":"Jul 22",
      "target_formatted":"",
      "change":0.0,
      "gapperc_formatted":"",
      "query":"opened_atONToday@javascript:gs.beginningOfToday()@javascript:gs.endOfToday()^ORopened_at<javascript:gs.beginningOfToday()^resolved_atISEMPTY^ORresolved_at>javascript:gs.endOfToday()^state!=8",
      "realtime_enabled":true,
      "changeperc":0.0,
      "target":null,
      "unit": {
        "display_value":"#",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "type":"formatted",
        "value":"17b365e2d7320100ba986f14ce6103ad"
      },
      "value_formatted":"14",             // Score where Assignment Group=Unassigned
      "name":"Number of open incidents > Assignment Group = Unassigned",
      "gapperc":null,
      "change_formatted":"0",
      "favorite":false,
      "personal_target_formatted":""
    },
    {"indicator": {
      
      "element": {
        "display_value":"Software",
        "link":"https://<instance>.service-now.com/api/now/v1/table/sys_user_group/8a4dde73c6112278017a6a4baf547aa7",
        "value":"8a4dde73c6112278017a6a4baf547aa7"    // sys_id of element Software
      },
      ...
  
      "value_formatted":"6",                         // Score where Assignment Group: Software
      "name":"Number of open incidents > Assignment Group = Software",
      "gapperc":null,
      "change_formatted":"0",
      "favorite":false,
      "personal_target_formatted":""
    },
    {"indicator": {
      ...
   
      "element": {
        "display_value":"Service Desk",
        "link":"https://<instance>.service-now.com/api/now/v1/table/sys_user_group/d625dccec0a8016700a222a0f7900d06",
        "value":"d625dccec0a8016700a222a0f7900d06"   // sys_id of element Service Desk
      },
  
      ...
      
      "value_formatted":"5",                        // Score for Assignment Group: Service Desk
      "name":"Number of open incidents > Assignment Group = Service Desk",
      "gapperc":null,
      "change_formatted":"0",
      "favorite":false,
      "personal_target_formatted":""
    },
    {"indicator": {
  
      ...
      
      "element": {
        "display_value":"Hardware",
        "link":"https://<instance>.service-now.com/api/now/v1/table/sys_user_group/8a5055c9c61122780043563ef53438e3",
        "value":"8a5055c9c61122780043563ef53438e3"   // sys_id for element Hardware
      },
  
      ...
      
      "value_formatted":"3",                         // Score for Assignment Group: Hardware
      "name":"Number of open incidents > Assignment Group = Hardware",
      "gapperc":null,
      "change_formatted":"0",
      "favorite":false,
      "personal_target_formatted":""
    },
    {"indicator": {
  
  ...

      "element": {
        "display_value":"Network",
        "link":"https://<instance>.service-now.com/api/now/v1/table/sys_user_group/287ebd7da9fe198100f92cc8d1d2154e",
        "value":"287ebd7da9fe198100f92cc8d1d2154e"},  // sys_id for element Network
  
... 

      "value_formatted":"3",                          // Score for Assignment Group: Network
      "name":"Number of open incidents > Assignment Group = Network",
      "gapperc":null,
      "change_formatted":"0",
      "favorite":false,
      "personal_target_formatted":""
    },
  ...
  ]
...
}

```

## Return the indicator filtered by a breakdown and element

You can apply a breakdown by appending the breakdown and breakdown element sys\_id values to the **sysparm\_uuid** parameter. In this example, the data is broken down to show priority 1 incidents. The sys\_id for the Priority breakdown is `0df47e02d7130100b96d45a3ce610399` and is in the example Return all breakdowns and aggregates for an indicator. You can get the sys\_id for the 1 - Critical element by running the same command as in Return all elements for a breakdown, but with the Priority breakdown instead of Assignment Group. The sys\_id for 1 - Critical is `5f012106db5123003ee8f93baf9619bd`.

Command:

```
curl -v -u "user:password" -H "Accept:application/json" "https://instance.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4:0df47e02d7130100b96d45a3ce610399:5f012106db5123003ee8f93baf9619bd"
```

Response:

```
{
// The request is made Dec 12. The
// score is 76, which is unchanged from
// Dec 11, and which exceeds the
// target of 70.
  "result": [ 
    { 
      "indicator": {
        "display_value":"Number of open incidents",
        "link":"https://instance.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value":"fb007202d7130100b96d45a3ce6103b4"
      },
      "gap_formatted":"-6",
      "benchmarking":false,
      "frequency_label":"Daily",
      "changeperc_formatted":"0.0%",
      "direction_label":"Minimize",
      "precision":0,
      "breakdown": {
        "display_value":"Priority",
        "link":"https://instance.service-now.com/api/now/v1/table/pa_breakdowns/0df47e02d7130100b96d45a3ce610399",
        "value":"0df47e02d7130100b96d45a3ce610399"
      },
      "personal_target":null,
      "description":"Number of incidents open based on resolved date is empty.",
      "value_color":"#ff8c00",
      "uuid":"fb007202d7130100b96d45a3ce6103b4:0df47e02d7130100b96d45a3ce610399:5f012106db5123003ee8f93baf9619bd",
      "frequency":10,
      "gap":-6.0,
      "value_unit":"76",
      "indicator_frequency":10,
      "value":76.0,
      "indicator_aggregate":1,
      "facts_table": {
        "name":"incident",
        "label":"Incidents"
      },
      "key":false,
      "indicator_frequency_label":"Daily",
      "direction":2,
      "element": {
        "display_value":"1 - Critical",
        "link":"https://instance.service-now.com/api/now/v1/table/sys_choice/5f012106db5123003ee8f93baf9619bd",
        "value":"5f012106db5123003ee8f93baf9619bd"
      },
      "period_title":"Dec 12",
      "period":"Dec 12",
      "target_formatted":"70",
      "change":0.0,
      "gapperc_formatted":"-8.6%",
      "query":"opened_atONToday@javascript:gs.beginningOfToday()@javascript:gs.endOfToday()^ORopened_at<javascript:gs.beginningOfToday()^resolved_atISEMPTY^ORresolved_at>javascript:gs.endOfToday()^state!=8^priority=1^EQ",
      "realtime_enabled":true,
      "changeperc":0.0,
      "target":70.0,
      "unit": {
        "display_value":"#",
        "link":"https://instance.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "type":"formatted","value":"17b365e2d7320100ba986f14ce6103ad"
      },
      "value_formatted":"76",
      "name":"Number of open incidents > Priority = 1 - Critical",
      "gapperc":-0.08571428571428572,
      "change_formatted":"0",
      "favorite":true,
      "personal_target_formatted":""
    }
  ]
}
```

## Return the indicator broken down by location

The Performance Analytics API returns geolocation data when available.

Command:

```
curl -v -u "user:password" -H "Accept:application/json" "https://<instance>.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4&sysparm_breakdown=656d5662eb23310065deac6aa206fee7"
```

Response:

```
{
  "result": [
    {
      ...
      "element": {
        "display_value": "San Diego",
        "link": "https://<instance>.service-now.com/api/now/v1/table/cmn_location/108752c8c611227501d4ab0e392ba97f",
        "value": "108752c8c611227501d4ab0e392ba97f",
        "longitude": -117.15726,
        "latitude": 32.71533
      },
      ...
    }
    {
      ...
      "element": {
        "display_value": "Florida",
        "link": "https://<instance>.service-now.com/api/now/v1/table/cmn_location/8e3e85f037d0200044e0bfc8bcbe5d14",
        "value": "8e3e85f037d0200044e0bfc8bcbe5d14",
        "longitude": -95.71289,
        "latitude": 37.09024
      },
      ...
    }
  ]
}
```

## Return first- and second-level breakdown scores

You can apply multiple breakdowns by appending multiple breakdown sys\_ids to the **sysparm\_uuid** parameter. In this example, the data is broken down by priority to show priority 1 incidents, and by category to show database incidents.

Command:

```
curl -v -u "user:password" -H "Accept:application/json" "https://instance.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4:0df47e02d7130100b96d45a3ce610399:e5900140200331007665978299a805f3:1f918835d7231100b96d45a3ce6103fe:9e418d40200331007665978299a805c1"
```

Response:

```
{
  "result": [
    {
      "value_formatted": "",
      "indicator": {
        "display_value": "Number of open incidents",
        "link": "http://instance.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value": "fb007202d7130100b96d45a3ce6103b4"
      },
      "gapperc": null,
      "change": null,
      "value_color": "#000000",
      "direction": 2,
      "target_formatted": "",
      "frequency": 10,
      "changeperc_formatted": "",
      "direction_label": "Minimize",
      "period_title": null,
      "description": "Number of incidents open based on resolved date is empty.",
      "name": "Number of open incidents / Priority / 1 - Critical / Category / Database",
      "value": null,
      "key": false,
      "gap_formatted": "",
      "element": {
        "display_value": "1 - Critical",
        "link": "http://instance.service-now.com/api/now/v1/table/sys_choice/e5900140200331007665978299a805f3",
        "value": "e5900140200331007665978299a805f3"
      },
      "precision": 0,
      "element_level2": {
        "display_value": "Database",
        "link": "http://instance.service-now.com/api/now/v1/table/sys_choice/9e418d40200331007665978299a805c1",
        "value": "9e418d40200331007665978299a805c1"
      },
      "breakdown": {
        "display_value": "Priority",
        "link": "http://instance.service-now.com/api/now/v1/table/pa_breakdowns/0df47e02d7130100b96d45a3ce610399",
        "value": "0df47e02d7130100b96d45a3ce610399"
      },
      "period": null,
      "favorite": false,
      "change_formatted": "",
      "unit": {
        "display_value": "#",
        "link": "http://instance.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value": "17b365e2d7320100ba986f14ce6103ad"
      },
      "frequency_label": "Daily",
      "breakdown_level2": {
        "display_value": "Category",
        "link": "http://instance.service-now.com/api/now/v1/table/pa_breakdowns/1f918835d7231100b96d45a3ce6103fe",
        "value": "1f918835d7231100b96d45a3ce6103fe"
      },
      "target": null,
      "changeperc": null,
      "uuid": "fb007202d7130100b96d45a3ce6103b4:0df47e02d7130100b96d45a3ce610399:e5900140200331007665978299a805f3:1f918835d7231100b96d45a3ce6103fe:9e418d40200331007665978299a805c1",
      "gapperc_formatted": "",
      "value_unit": "",
      "gap": null
    }
  ]
}
```

## Return scores across a range of dates for two levels of breakdown

You can request a list of individual scores for all available dates by setting the **sysparm\_include\_scores** parameter to true. To specify the date range of scores, also use the **sysparm\_from** and **sysparm\_to** parameters. In this example, the level 1 breakdown and element are Assignment Group: Software \(sys\_id `baec0752bf130100b96dac808c0739ed` and `8a4dde73c6112278017a6a4baf547aa7`\). The level 2 breakdown and element are Priority: 1 - Critical \(sys\_id `0df47e02d7130100b96d45a3ce610399` and `e5900140200331007665978299a805f3`\). Only scores on and after 30 November 2018 are returned.

Command:

```
curl -v -u "resttest:resttest" -H "Accept:application/json" "https://<instance>.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:8a4dde73c6112278017a6a4baf547aa7:0df47e02d7130100b96d45a3ce610399:e5900140200331007665978299a805f3&sysparm_include_scores=true&sysparm_from=2018-11-30"
```

Response:

```
{
  "result": [
    { "indicator": {
        "display_value":"Number of open incidents",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value":"fb007202d7130100b96d45a3ce6103b4"
      },
      "gap_formatted":"",
      "benchmarking":false,
      "frequency_label":"Daily",
      "scores": [
        { "end_at":"2018-12-04",
          "period":"Dec 04",
          "value_formatted":"2",
          "start_at":"2018-12-04",
          "value":2.0
        },
        ...
       
        { "end_at":"2018-11-30",
          "period":"Nov 30",
          "value_formatted":"0",
          "start_at":"2018-11-30",
          "value":0.0
        }
      ],
      "changeperc_formatted":"",
      "direction_label":"Minimize",
      "precision":0,
      "breakdown": {                      //First-level breakdown
        "display_value":"Assignment Group",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_breakdowns/baec0752bf130100b96dac808c0739ed",
        "value":"baec0752bf130100b96dac808c0739ed"
      },
      "personal_target":null,
      "description":"Number of incidents open based on resolved date is empty.",
      "value_color":"#455464",
      "uuid":"fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:8a4dde73c6112278017a6a4baf547aa7:0df47e02d7130100b96d45a3ce610399:e5900140200331007665978299a805f3",
      "frequency":10,
      "gap":null,
      "value_unit":"2",
      "indicator_frequency":10,
      "value":2.0,
      "indicator_aggregate":1,
      "key":false,
      "indicator_frequency_label":"Daily",
      "direction":2,
      "element": {                        //First-level breakdown element
        "display_value":"Software",
        "link":"https://<instance>.service-now.com/api/now/v1/table/sys_user_group/8a4dde73c6112278017a6a4baf547aa7",
        "value":"8a4dde73c6112278017a6a4baf547aa7"
      },
      "period_title":"Dec 04",
      "period":"Dec 04",
      "target_formatted":"",
      "change":2.0,
      "gapperc_formatted":"",
      "realtime_enabled":false,
      "changeperc":null,
      "target":null,
      "unit":{ 
        "display_value":"#",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "type":"formatted",
        "value":"17b365e2d7320100ba986f14ce6103ad"
      },
      "value_formatted":"2",               //Second-level breakdown and element
      "name":"Number of open incidents > Assignment Group = Software > Priority = e5900140200331007665978299a805f3",
      "gapperc":null,
      "change_formatted":"2",
      "favorite":false,
      "breakdown_level2": {
        "display_value":"Priority",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_breakdowns/0df47e02d7130100b96d45a3ce610399",
        "value":"0df47e02d7130100b96d45a3ce610399"
      },
      "personal_target_formatted":""
    }
  ]
}
```

## Return breakdown relations for a breakdown and element

To obtain the sys\_id values for all breakdown relations associated with an indicator, use the **sysparm\_include\_available\_breakdowns** parameter. In the **sysparm\_uuid** parameter, include the sys\_ids of the first-level breakdown and element whose relations you want to find. In this example, the **sysparm\_uuid** parameter includes the sys\_id for the Assignment Group breakdown and the sys\_id for the Software element. The sys\_id of the Assignment Group was obtained in the example where all breakdowns and aggregates were returned. The sys\_id of the Software element was obtained in the previous example, where all the elements of Assignment Group were returned. The sys\_id of the Assignment Group breakdown is `baec0752bf130100b96dac808c0739ed` and of the Software element is `8a4dde73c6112278017a6a4baf547aa7`. The breakdown relation is obtained for the Number of open incidents indicator, whose sys\_id is `fb007202d7130100b96d45a3ce6103b4`.

**Note:** To find the breakdown relations for incidents that do not match any element value in a breakdown, such as in Assignment Group: Unassigned, use the string `unmatched` in place of the element sys\_id. In this case, the parameter would be `sysparm_uuid=fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:unmatched`.

Command:

```
curl -v -u "user:password" -H "Accept:application/json" "https://<instance>.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:8a4dde73c6112278017a6a4baf547aa7&sysparm_include_available_breakdowns=true"
```

Response:

```
{
  "result": [
    {
      "value_formatted": "37",
      "indicator": {
        "display_value": "Number of open incidents",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value": "fb007202d7130100b96d45a3ce6103b4"
      },
      "gapperc": null,
      "change": 9.0,
      "value_color": "#455464",
      "direction": 2,
      "target_formatted": "",
      "frequency": 10,
      "changeperc_formatted": "32.1%",
      "direction_label": "Minimize",
      "period_title": "Jul 22",
      "description": "Number of incidents open based on resolved date is empty.",
      "name": "Number of open incidents / Assignment Group / Software",
      "value": 37.0,
      "key": false,
      "gap_formatted": "",
      "element": {
        "display_value": "Software",
        "link": "https://<instance>.service-now.com/api/now/v1/table/sys_user_group/287ee6fea9fe198100ada7950d0b1b73",
        "value": "8a4dde73c6112278017a6a4baf547aa7"
      },
      "precision": 0,
      "breakdowns": [
        // Information about each breakdown
        
      ],
      "breakdown_relations": [
        {
          "display_value": "Child Groups",
          "link": "https://<instance>.service-now.com/api/now/v1/table/pa_breakdown_relations/301fd511eb23310065deac6aa206fe31",
          "value": "301fd511eb23310065deac6aa206fe31"
        },
        {
          "display_value": "Parent Group",
          "link": "https://<instance>.service-now.com/api/now/v1/table/pa_breakdown_relations/790b6e11eb23310065deac6aa206fe1c",
          "value": "790b6e11eb23310065deac6aa206fe1c"
        },
        {
          "display_value": "Sibling Groups",
          "link": "https://<instance>.service-now.com/api/now/v1/table/pa_breakdown_relations/15e15a12eb233100871aac6aa206fe59",
          "value": "15e15a12eb233100871aac6aa206fe59"
        }
      ],
      "breakdown": {
        "display_value": "Assignment Group",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_breakdowns/baec0752bf130100b96dac808c0739ed",
        "value": "baec0752bf130100b96dac808c0739ed"
      },
      "period": "Jul 22",
      "favorite": false,
      "change_formatted": "9",
      "unit": {
        "display_value": "#",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value": "17b365e2d7320100ba986f14ce6103ad"
      },
      "frequency_label": "Daily",
      "target": null,
      "changeperc": 0.32142857142857145,
      "uuid": "fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:8a4dde73c6112278017a6a4baf547aa7",
      "gapperc_formatted": "",
      "value_unit": "6",
      "gap": null
    }
  ]
}
```

## Return indicator using a breakdown relation

To use a breakdown relation, include the sys\_id values of the indicator, breakdown, and element in the **sysparm\_uuid** parameter, and the sys\_id of the breakdown relation in the **sysparm\_breakdown\_relation** parameter. This example returns the Sibling Group values for Assignment Group: Software from the previous example.

Command:

```
curl -v -u "user:password" -H "Accept:application/json" "https://<instance>.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:8a4dde73c6112278017a6a4baf547aa7&sysparm_breakdown_relation=15e15a12eb233100871aac6aa206fe59"
```

Response:

```
{
  "result": [
    {
      "indicator": {
      "gap_formatted":"",
      "benchmarking":false,
      "frequency_label":"Daily",
      "changeperc_formatted":"0.0%",
      "direction_label":"Minimize",
      "precision":0,
      "breakdown": {
        "display_value":"Assignment Group",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_breakdowns/baec0752bf130100b96dac808c0739ed",
        "value":"baec0752bf130100b96dac808c0739ed"
      },
      "personal_target":null,
      "description":"Number of incidents open based on resolved date is empty",
      "value_color":"#455464",
      "uuid":"fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:0a52d3dcd7011200f2d224837e6103f2",
      "frequency":10,
      "gap":null,
      "value_unit":"0",
      "indicator_frequency":10,
      "value":0.0,
      "indicator_aggregate":1,
      "facts_table": {
        "name":"incident",
        "label":"Incidents"
      },
      "key":false,
      "indicator_frequency_label":"Daily",
      "direction":2,
      "element": {
        "display_value":"Application Development",
        "link":"https://<instance>.service-now.com/api/now/v1/table/sys_user_group/0a52d3dcd7011200f2d224837e6103f2",
        "value":"0a52d3dcd7011200f2d224837e6103f2"
      },
      "period_title":"Dec 03",
      "period":"Dec 03",
      "target_formatted":"",
      "change":0.0,
      "gapperc_formatted":"",
      "query":"opened_atONToday@javascript:gs.beginningOfToday()@javascript:gs.endOfToday()^ORopened_at<javascript:gs.beginningOfToday()^resolved_atISEMPTY^ORresolved_at>javascript:gs.endOfToday()^state!=8^assignment_group=0a52d3dcd7011200f2d224837e6103f2^EQ",
      "realtime_enabled":true,
      "changeperc":0.0,
      "target":null,
      "unit": {
        "display_value":"#",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "type":"formatted",
        "value":"17b365e2d7320100ba986f14ce6103ad"
      },
      "value_formatted":"0",
      "name":"Number of open incidents > Assignment Group = Application Development",
      "gapperc":null,
      "change_formatted":"0",
      "favorite":false,
      "personal_target_formatted":""
    }
    // Followed by an indicator object with an element object for every element in the Sibling Group
  ]
}
```

## Return a filtered set of elements for a breakdown

You can apply a filter to the Analytics Hub data using the **sysparm\_elements\_filter** parameter with the sys\_id of a Performance Analytics element filter record.

Get the sys\_id of the elements filter from the elements filter record, as described in .

In this example, the element filter applies to the Groups breakdown source, with the condition \[\[Parent\]\[is\]\[Database\]\]. The sys\_id of this element filter is `7b9eb563eb11020065deac6aa206fe11`. The example gets the elements of the Assignment Group breakdown that have the element Database as a parent.

Command:

```
curl -v -u "user:password" -H "Accept:application/json" "https://<instance>.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4&sysparm_breakdown=baec0752bf130100b96dac808c0739ed&sysparm_elements_filter=7b9eb563eb11020065deac6aa206fe11"
```

Response:

```
{
  "result": [
    {
      "value_formatted": "37",
      "indicator": {
        "display_value": "Number of open incidents",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value": "fb007202d7130100b96d45a3ce6103b4"
      },
      "gapperc": null,
      "change": 9.0,
      "value_color": "#455464",
      "direction": 2,
      "target_formatted": "",
      "frequency": 10,
      "changeperc_formatted": "32.1%",
      "direction_label": "Minimize",
      "period_title": "Jul 22",
      "description": "Number of incidents open based on resolved date is empty.",
      "name": "Number of open incidents / Assignment Group / Database",
      "value": 37.0,
      "key": false,
      "gap_formatted": "",
      "element": {
        "display_value": "Database",
        "link": "https://<instance>.service-now.com/api/now/v1/table/sys_user_group/287ee6fea9fe198100ada7950d0b1b73",
        "value": "287ee6fea9fe198100ada7950d0b1b73"
      },
      "precision": 0,
      "breakdown": {
        "display_value": "Assignment Group",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_breakdowns/baec0752bf130100b96dac808c0739ed",
        "value": "baec0752bf130100b96dac808c0739ed"
      },
      "period": "Jul 22",
      "favorite": false,
      "change_formatted": "9",
      "unit": {
        "display_value": "#",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value": "17b365e2d7320100ba986f14ce6103ad"
      },
      "frequency_label": "Daily",
      "target": null,
      "changeperc": 0.32142857142857145,
      "uuid": "fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:287ee6fea9fe198100ada7950d0b1b73",
      "gapperc_formatted": "",
      "value_unit": "37",
      "gap": null
    },
    {
      "value_formatted": "20",
      "indicator": {
        "display_value": "Number of open incidents",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value": "fb007202d7130100b96d45a3ce6103b4"
      },
      // Database Atlanta
      "gapperc": null,
      "change": 4.0,
      "value_color": "#455464",
      "direction": 2,
      "target_formatted": "",
      "frequency": 10,
      "changeperc_formatted": "25.0%",
      "direction_label": "Minimize",
      "period_title": "Jul 22",
      "description": "Number of incidents open based on resolved date is empty.",
      "name": "Number of open incidents / Assignment Group / Database Atlanta",
      "value": 20.0,
      "key": false,
      "gap_formatted": "",
      "element": {
        "display_value": "Database Atlanta",
        "link": "https://<instance>.service-now.com/api/now/v1/table/sys_user_group/db53580b0a0a0a6501aa37c294a2ba6b",
        "value": "db53580b0a0a0a6501aa37c294a2ba6b"
      },
      "precision": 0,
      "breakdown": {
        "display_value": "Assignment Group",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_breakdowns/baec0752bf130100b96dac808c0739ed",
        "value": "baec0752bf130100b96dac808c0739ed"
      },
      "period": "Jul 22",
      "favorite": false,
      "change_formatted": "4",
      "unit": {
        "display_value": "#",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value": "17b365e2d7320100ba986f14ce6103ad"
      },
      "frequency_label": "Daily",
      "target": null,
      "changeperc": 0.25,
      "uuid": "fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:db53580b0a0a0a6501aa37c294a2ba6b",
      "gapperc_formatted": "",
      "value_unit": "20",
      "gap": null
    },
    {
      "value_formatted": "19",
      "indicator": {
        "display_value": "Number of open incidents",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value": "fb007202d7130100b96d45a3ce6103b4"
      },
      ...
      
      // Database San Diego
      "gapperc": null,
      "change": 0.0,
      "value_color": "#455464",
      "direction": 2,
      "target_formatted": "",
      "frequency": 10,
      "changeperc_formatted": "0.0%",
      "direction_label": "Minimize",
      "period_title": "Jul 22",
      "description": "Number of incidents open based on resolved date is empty.",
      "name": "Number of open incidents / Assignment Group / Database San Diego",
      "value": 10.0,
      "key": false,
      "gap_formatted": "",
      "element": {
        "display_value": "Database San Diego",
        "link": "https://<instance>.service-now.com/api/now/v1/table/sys_user_group/db53a9290a0a0a650091abebccf833c6",
        "value": "db53a9290a0a0a650091abebccf833c6"
      },
      "precision": 0,
      "breakdown": {
        "display_value": "Assignment Group",
        "link": "http://localhost:8080/api/now/v1/table/pa_breakdowns/baec0752bf130100b96dac808c0739ed",
        "value": "baec0752bf130100b96dac808c0739ed"
      },
      "period": "Jul 22",
      "favorite": false,
      "change_formatted": "0",
      "unit": {
        "display_value": "#",
        "link": "http://<instance>.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value": "17b365e2d7320100ba986f14ce6103ad"
      },
      "frequency_label": "Daily",
      "target": null,
      "changeperc": 0.0,
      "uuid": "fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:db53a9290a0a0a650091abebccf833c6",
      "gapperc_formatted": "",
      "value_unit": "10",
      "gap": null
    }
  ]
}
```

**Parent Topic:**[Integrate Performance Analytics](../../../use/performance-analytics/concept/c_PAWebServiceIntegrations.md)

