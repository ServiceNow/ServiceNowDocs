---
title: OCRosterSpanApprovalUtil - Global
description: The OCRosterSpanApprovalUtil script include provides methods for the PTO approval feature.Changes the type of the roster\_schedule\_span to time-off from approval.Returns a URL to the on-call calendar based on the rosterSpanProposalGr.Returns a formatted GlideScheduleDateTime string based on the start date of the rosterSpanProposalGr.Returns an array of group managers based on the user's rota groups.Returns a formatted GlideScheduleDateTime string based on the end date of the rosterSpanProposalGr.Returns the user's name based on rosterSpanProposalGr.Checks whether the system property com.snc.on\_call\_rotation.pto.approval.required is true.Changes the type of the roster\_schedule\_span to rejected from approval.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# OCRosterSpanApprovalUtil- Global

The OCRosterSpanApprovalUtil script include provides methods for the PTO approval feature.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## OCRosterSpanApprovalUtil - approvePTOSpan \(GlideRecord rosterSpanGr\)

Changes the type of the roster\_schedule\_span to time-off from approval.

|Name|Type|Description|
|----|----|-----------|
|rosterSpanGr|GlideRecord|A roster\_schedule\_span\_proposal record.|

|Type|Description|
|----|-----------|
|void| |

## OCRosterSpanApprovalUtil - getContextualCalUrlPerSpanProposal \(GlideRecord rosterSpanProposalGr\)

Returns a URL to the on-call calendar based on the rosterSpanProposalGr.

|Name|Type|Description|
|----|----|-----------|
|rosterSpanProposalGr|GlideRecord|A roster\_schedule\_span\_proposal record.|

|Type|Description|
|----|-----------|
|String|A URL to the on-call calendar based on the rosterSpanProposalGr.|

## OCRosterSpanApprovalUtil - getFromDateDisplayValuePerSpanProposal \(GlideRecord rosterSpanProposalGr\)

Returns a formatted GlideScheduleDateTime string based on the start date of the rosterSpanProposalGr.

|Name|Type|Description|
|----|----|-----------|
|rosterSpanProposalGr|GlideRecord|A roster\_schedule\_span\_proposal record.|

|Type|Description|
|----|-----------|
|String|A formatted GlideScheduleDateTime string based on the start date of the rosterSpanProposalGr.|

## OCRosterSpanApprovalUtil - getPTOApproversList\(GlideRecord rosterSpanProposalGr\)

Returns an array of group managers based on the user's rota groups.

|Name|Type|Description|
|----|----|-----------|
|rosterSpanProposalGr|GlideRecord|A roster\_schedule\_span\_proposal record.|

|Type|Description|
|----|-----------|
|Array|An array of group managers based on the user's rota groups.|

The following example is an on-demand script include named OCPTOApprovalReminder. When called by running the scheduled job manually, the managers and their delegate managers are notified of employees who are scheduled for PTO on the following day.

```
function OCPTOApprovalReminder() {

	//Passing parameters in 'getDateFormat()' function with the days which needs to be added
	var startDate = getDateFormat(1); //We can use System property to set Start Date
	var endDate = getDateFormat(2); //We can use System property to set End Date
	
	//Building the encoded query all the Pending approval state proposals whose start date is tomorrow
	var encodedQuery = 'state=1^roster_schedule_span.start_date_time>' + startDate + '^roster_schedule_span.start_date_time<' + endDate;
	
	//Sends an event notification to all rota managers and their delegate managers
	getNotApprovedList(encodedQuery);
	
	//Converts the date and time in ISO Format
	function getDateFormat(daysToBeAdded) {

		//Getting today's date and adding '1' day
		var todaysDate = new GlideDate();
		todaysDate.addDaysUTC(daysToBeAdded);
		todaysDate = todaysDate.getValue();

		//Converting to today's date object to GlideDate object
		var addingDaysToDate = new GlideDate();
		addingDaysToDate.setValue(todaysDate);

		//Setting the time default to '12:00:00' and returning the time in the specified format to match ISO
		var staticTime = new GlideTime();
		staticTime.setValue('00:00:00');
		staticTime.setValue(staticTime.getHourOfDayUTC() + ':' + staticTime.getMinutesUTC() + ':' + staticTime.getSeconds());

		//Returns the date & time in the specified format
		var isoFormattedDateTime = addingDaysToDate.getByFormat("yyyyMMdd") + 'T' + staticTime.getByFormat("HHmmss") + 'Z';
		return isoFormattedDateTime;
	}
	
	//Gliding Roster schedule span proposal table with the built-in query to fetch the records whose proposals are not approved/rejected
	function getNotApprovedList(addEncodedQuery) {
		var rosterScheduleEntryProposalGR = new GlideRecord('roster_schedule_span_proposal');
		rosterScheduleEntryProposalGR.addEncodedQuery(addEncodedQuery);
		rosterScheduleEntryProposalGR.query();
		while(rosterScheduleEntryProposalGR.next()) {

			//Call On-Call Scheduling OCRosterSpanApprovalUtil library with 'getPTOApproversList' function 
			//pass GlideRecord object of 'roster_schedule_span_proposal' table
			var rotaManagers = new OCRosterSpanApprovalUtil().getPTOApproversList(rosterScheduleEntryProposalGR);
			rotaManagers = rotaManagers.join(",");

			// Pull only the unique sys_ids
			var managerList = new ArrayUtil().unique(getManagerDelegateApprovals(rotaManagers).toString().split(','));

                     // Event to trigger a reminder notification for testing.
                     // To use, create a an event registry named "oc.manager.delegate.reminder"
                     // Call the event in a notification and uncomment the following line
			//gs.eventQueue("oc.manager.delegate.reminder", rosterScheduleEntryProposalGR, managerList, "");

               if(managerList)
			gs.info("Returns the list of manager and it's delegate members >>>>>> " + managerList);
		}
	}
	
	//Get the sys_ids of the managers and their delegate managers
	function getManagerDelegateApprovals(manager) {
		var answer = [];
        answer.push(manager);
		var delegateGR = new GlideRecord("sys_user_delegate");
		delegateGR.addQuery("user", 'IN', manager);
		delegateGR.addQuery("starts", "<=", gs.daysAgo(0));
		delegateGR.addQuery("ends", ">=", gs.daysAgo(0));
		delegateGR.addQuery("approvals", true);
		delegateGR.query();
		while(delegateGR.next()) {
			answer.push(delegateGR.getValue('user'));
			answer.push(delegateGR.getValue('delegate'));
		}
		return answer;
	}
}
```

Add the following call to a record in the Scheduled Script Execution \[sysauto\_script\] table. This trigger calls the OCPTOApprovalReminder script include when the scheduled job is run manually.

```
OCPTOApprovalReminder();
```

## OCRosterSpanApprovalUtil - getToDateDisplayValuePerSpanProposal \(rosterSpanProposalGr GlideRecord\)

Returns a formatted GlideScheduleDateTime string based on the end date of the rosterSpanProposalGr.

|Name|Type|Description|
|----|----|-----------|
|rosterSpanProposalGr|GlideRecord|A roster\_schedule\_span\_proposal record.|

|Type|Description|
|----|-----------|
|String|A formatted GlideScheduleDateTime string based on the end date of the rosterSpanProposalGr.|

## OCRosterSpanApprovalUtil - getUserNamePerSpanProposal \(GlideRecord rosterSpanProposalGr\)

Returns the user's name based on rosterSpanProposalGr.

|Name|Type|Description|
|----|----|-----------|
|rosterSpanProposalGr|GlideRecord|A roster\_schedule\_span\_proposal record.|

|Type|Description|
|----|-----------|
|String|The user's name based on rosterSpanProposalGr.|

## OCRosterSpanApprovalUtil - isPTOApprovalRequired \(\)

Checks whether the system property **com.snc.on\_call\_rotation.pto.approval.required** is true.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns true if the system property **com.snc.on\_call\_rotation.pto.approval.required** is true..|

## OCRosterSpanApprovalUtil - rejectPTOSpan \(rosterSpanGr GlideRecord\)

Changes the type of the roster\_schedule\_span to rejected from approval.

|Name|Type|Description|
|----|----|-----------|
|rosterSpanGr|GlideRecord|A roster\_schedule\_span\_proposal record.|

|Type|Description|
|----|-----------|
|void| |

