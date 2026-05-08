---
title: hr\_ActivitySet - Scoped
description: The hr\_ActivitySet API handles lifecycle event activity set cases.Instantiates an instance of the hr\_ActivitySet class.Creates a lifecycle event case based on a specified HR service.Checks for a case matching the specified combination of subject person user, HR service, and job.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# hr\_ActivitySet- Scoped

The hr\_ActivitySet API handles lifecycle event activity set cases.

Lifecycle event activity sets represent different stages in the lifecycle event process. You must define when the activity set is triggered, such as immediately upon creation of the lifecycle event case or after the completion of another activity set. Each activity set is associated with a single lifecycle event.

The hr\_ActivitySet API requires the HR Lifecycle Events plugin \(com.sn\_hr\_lifecycle\_events\) and runs in the `sn_hr_le` namespace.

For additional information, see Understanding Enterprise Onboarding and Transitions.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## hr\_ActivitySet - hr\_ActivitySet\(\)

Instantiates an instance of the hr\_ActivitySet class.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## hr\_ActivitySet - createLECaseByService\(String hrService, Object caseValues\)

Creates a lifecycle event case based on a specified HR service.

|Name|Type|Description|
|----|----|-----------|
|hrService|String|Sys ID of HR service in the HR Services \[sn\_hr\_core\_service\] table to be assigned to the lifecycle event case.|
|caseValues|Object|Key-value pairs containing a value for each case field.|
|caseValues.subject\_person|String|Sys ID of subject person's name in the User \[sys\_user\] table.|
|caseValues.opened\_for|String|Sys ID of case opened for subject person in the Users \[sys\_user\] table.|
|caseValues.subject\_person\_job|String|Sys ID of subject person's Business title in the Jobs \[sn\_hr\_core\_job\] table.|
|caseValues.location|String|Sys ID of subject person's location in HR profile in the Locations \[cmn\_location\] table.|
|caseValues.department|String|Sys ID of subject person's department in HR profile in the Departments \[cmn\_department\] table.|
|caseValues.subject\_person\_hr\_profile|String|Sys ID of subject person's HR profile in the HR Profiles \[sn\_hr\_core\_profile\] table.|
|caseValues.short\_description|String|Case description.|
|caseValues.state|Number|Number representing uniquely-defined custom case state.|

|Type|Description|
|----|-----------|
|String|Sys ID of the created case in the HR Lifecycle Events Cases \[sn\_hr\_le\_case\] table.|

Output includes summary with Operation Table and Row Count columns. Click the link in the row count column adjacent sn\_hr\_le\_case table to view the new case.

```
var caseValues = {
              'subject_person': '62826bf03710200044e0bfc8bcbe5df1',
              'opened_for': '0e826bf03710200044e0bfc8bcbe5d7c',
              'subject_person_job': 'f8d56900587d3700964f4efae452b3db',
              'location': '25ab9d1d0a0a0bb300537fd25687439d',
              'department': '93b25282c0a8000b0b55c8ab34e2f1e6',
              'subject_person_hr_profile': '330370019f22120047a2d126c42e7012',
              'short_description': 'Short description',
              'state': 10
          };

  var activity = new sn_hr_le.hr_ActivitySet();
  var createCase = new activity.createLECaseByService('4719647c67a60300132a6c3b5685ef16', caseValues);
```

Output:

```
...
insert	sn_hr_le_case	1
...
```

## hr\_ActivitySet - hasActiveCaseByService\(String spUser, String hrService, String jobId\)

Checks for a case matching the specified combination of subject person user, HR service, and job.

|Name|Type|Description|
|----|----|-----------|
|spUser|String|Sys ID of subject person user in the Users \[sys\_user\] table.|
|hrService|String|Sys ID of HR service in the HR Services \[sn\_hr\_core\_service\] table.|
|jobId|String|Sys ID of subject user's job title in the HR Services \[sn\_hr\_core\_service\] table.|

|Type|Description|
|----|-----------|
|Boolean|True if matching case exists, false otherwise.|

```
var userId = '62826bf03710200044e0bfc8bcbe5df1'; //Abel Tuter
var hrServiceId = '64fa4c53534222003066a5f4a11c0875'; //Onboarding HR Service
var jobId = '3D62826bf03710200044e0bfc8bcbe5df1'; // Sample Job sys_id for the example

var activity = new sn_hr_le.hr_ActivitySet();

var hasActiveLECase = activity.hasActiveCaseByService(userId, hrServiceId, jobId);

gs.info('User has an active HR case: ' + hasActiveLECase);
```

Output:

```
sn_hr_le: User has an active HR case: false
```

