---
title: Configure the header message on the landing page
description: Configure the header message that is part of the greeting text on the landing page. For example, You are on-call until Monday, Mar 21.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Landing page configurations in SOW for ITSM, Getting started, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the header message on the landing page

Configure the header message that is part of the greeting text on the landing page. For example, You are on-call until Monday, Mar 21.

## Before you begin

Role required: admin

## About this task

The Get service desk agent shift data broker server script calls the `SOWServiceDeskAgentShift` script includes to display the shift information in the greeting text.

While the display text can be customized for the default landing page, the visual styling changes to the text can be done only by creating a copy of the landing page.

![Greeting text.](../image/greeting-text.png "Header section")

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Overview**.

2.  On the **Overview** tab, from the **Initial Setup** section, select the **Configure the landing page** option.

3.  On the Landing Page form, select **Configure** next to **Greetings**.

    The Script Includes form is displayed for SOWServiceDeskAgentShift, which internally calls the SOWServiceDeskAgentShiftSNC

4.  Copy the **Script** value of SOWServiceDeskAgentShiftSNC.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

    2.  From the list of Script Includes, open SOWServiceDeskAgentShiftSNC.

    3.  Copy the **Script** field value.

5.  Edit the SOWServiceDeskAgentShift script.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

    2.  From the list of Script Includes, open SOWServiceDeskAgentShift.

    3.  Paste the **Script** field value that you copied from SOWServiceDeskAgentShiftSNC.

        ```
        initialize: function() { 
        
                this.PLUGINS = { 
        
                    ON_CALL: "com.snc.on_call_rotation", 
        
                    SHIFT_PLANNING: "com.sn_shift_planning" 
        
                }; 
        
                this.DAYS_AHEAD = gs.getProperty('com.snc.on_call_rotation.upcoming_rota_days', 30); 
        
                this.DATE_FORMAT = gs.getDateFormat(); 
        
                this.TIME_FORMAT = gs.getTimeFormat(); 
        
                this.WFO_SCHEMA_IDENTIFIER = 'readInTimezone'; 
        
                this.WFO_ONCALL_TYPE_IDENTIFIER = 'oncallAPIReadInTimezone'; 
        
                this.WEEK_DAY_FORMAT = 'EEEE'; 
        
                this.FORMAT = { 
        
                    SERVICE_DESK_HEADER: 'SERVICE_DESK_HEADER' 
        
                }; 
        
                this.DATE_TIME_FORMAT_FULL = "full"; 
        
            }, 
        
         
        
            getUpcomingShift: function(userId, outputFormat, wfoShift) { 
        
                var upcomingShifts, gd = new GlideDate(); 
        
                var from = gd.getDisplayValueInternal(); 
        
                gd.addDaysLocalTime(this.DAYS_AHEAD); 
        
                var to = gd.getDisplayValueInternal(); 
        
                var mayBeWFOUser = userId == gs.getUserID() ? gs.hasRole("sn_shift_planning.agent") : true; 
        
                if (GlidePluginManager.isActive(this.PLUGINS.SHIFT_PLANNING) && mayBeWFOUser && wfoShift) 
        
                    upcomingShifts = this.getWFOShifts(from, to, userId); 
        
                var isWFOResponseValid = Array.isArray(upcomingShifts) && upcomingShifts.length > 0; 
        
                if (!isWFOResponseValid && GlidePluginManager.isActive(this.PLUGINS.ON_CALL)) 
        
                    upcomingShifts = this.getOnCallShifts(from, to, userId); 
        
                return this.getFormattedShift(upcomingShifts, outputFormat); 
        
            }, 
        
         
        
            getWFOShifts: function(from, to, userId) { 
        
                var smUtil = new sn_shift_planning.ScheduleManagerUtil(); 
        
                var defaultEventCategories = [ 
        
                    smUtil.WORK_CATEGORY_SYS_ID, 
        
                    smUtil.ON_CALL_CATEGORY_SYS_ID 
        
                ]; 
        
                var params = { 
        
                    "assignmentGroups": "", 
        
                    "individualAgents": userId, 
        
                    "startDate": from, 
        
                    "endDate": to, 
        
                    "published": true, 
        
                    "eventCategories": defaultEventCategories, 
        
                    "filter": { 
        
                        "sn_shift_planning_agent_schedule": { 
        
                            "event": ["8d03fd9b0f310010717cc562ff767e4a", "936319993bd02010e81a4ee1f3efc419"] 
        
                        } 
        
                    } 
        
                }; 
        
                var upcomingShifts = []; 
        
                try { 
        
                    var agentScheduleRESTAPIUtils = new sn_shift_planning.AgentScheduleRESTAPIUtils(); 
        
                    var spans = agentScheduleRESTAPIUtils.retrieveAgentSchedulesFromParams(params); 
        
                    if (spans && spans.shiftData && spans.shiftData.user && spans.shiftData.user.data && spans.shiftData.user.data.length > 0 && spans.shiftData.user.data[0].schedules) { 
        
                        var schedules = spans.shiftData.user.data[0].schedules, 
        
                            arrayUtil = new global.ArrayUtil(); 
        
                        for (var schedule in schedules) 
        
                            upcomingShifts = arrayUtil.union(upcomingShifts, schedules[schedule]); 
        
                    } 
        
                } catch (e) { 
        
                    gs.error("SOWServiceDeskAgentShiftSNC: Error fetching WFO shifts"); 
        
                } 
        
         
        
                return upcomingShifts; 
        
            }, 
        
         
        
            getOnCallShifts: function(from, to, userId) { 
        
                var onCallCommon = new global.OnCallCommon(); 
        
                var onCallGroups = onCallCommon.getMyGroups(); 
        
                var spans = new global.OCRotationV2(null, global.OCRotationV2.DEFAULT_FORMAT_OPTION).setStartDate(from).setEndDate(to).setUserIds(userId).setGroupIds(onCallGroups).getSpans(); 
        
                var upcomingShifts = []; 
        
                for (var i = 0; i < spans.length; i++) 
        
                    if ((spans[i].type == "roster" || spans[i].type == "override") && spans[i].user_id == userId) 
        
                        upcomingShifts.push(spans[i]); 
        
                return upcomingShifts; 
        
            }, 
        
         
        
            getFormattedShift: function(upcomingShifts, outputFormat) { 
        
                if (gs.nil(upcomingShifts)) 
        
                    return; 
        
                switch (outputFormat) { 
        
                    case this.FORMAT.SERVICE_DESK_HEADER: 
        
                        return this.getServiceDeskFormattedShift(upcomingShifts); 
        
                    default: 
        
                        return upcomingShifts; 
        
                } 
        
            }, 
        
         
        
            getServiceDeskFormattedShift: function(upcomingShifts) { 
        
                var response = { 
        
                    shiftText: "", 
        
                    nearestShift: {} 
        
                }; 
        
                var startAttr = "start", 
        
                    endAttr = "end", 
        
                    isOnCall = true; 
        
                var dateFormat = 'EEEE, MMM dd', 
        
                    timeFormat = 'hh:mm a'; 
        
                var isWFOSchema = Array.isArray(upcomingShifts) && upcomingShifts.length > 0 && this.WFO_SCHEMA_IDENTIFIER in upcomingShifts[0]; 
        
                if (isWFOSchema) 
        
                    startAttr = "scheduledStartTime", endAttr = "scheduledEndTime"; 
        
                response.nearestShift = this.getNearestShift(upcomingShifts, startAttr, endAttr); 
        
                if (response.nearestShift) { 
        
                    if (isWFOSchema) { 
        
                        if (response.nearestShift.schedule && !(this.WFO_ONCALL_TYPE_IDENTIFIER in response.nearestShift.schedule)) 
        
                            isOnCall = false; 
        
                    } 
        
                    if (isOnCall) { 
        
                        if (response.nearestShift.isCurrent) { 
        
                            if (response.nearestShift.roster_name) 
        
                                response.shiftText = gs.getMessage("You are on-call until {0} as {1}", [this.getFormattedDateTime(response.nearestShift[endAttr]), response.nearestShift.roster_name]); 
        
                            else 
        
                                response.shiftText = gs.getMessage("You are on-call until {0}", [this.getFormattedDateTime(response.nearestShift[endAttr])]); 
        
                        } else { 
        
                            if (response.nearestShift.roster_name) 
        
                                response.shiftText = gs.getMessage("Your next on-call shift starts on {0} as {1}", [this.getFormattedDateTime(response.nearestShift[startAttr]), response.nearestShift.roster_name]); 
        
                            else 
        
                                response.shiftText = gs.getMessage("Your next on-call shift starts on {0}", [this.getFormattedDateTime(response.nearestShift[startAttr])]); 
        
                        } 
        
                    } else { 
        
                        if (response.nearestShift.isCurrent) { 
        
                            response.shiftText = gs.getMessage("Your shift ends on {0}", [this.getFormattedDateTime(response.nearestShift[endAttr])]); 
        
                        } else 
        
                            response.shiftText = gs.getMessage("Your next shift starts on {0}", [this.getFormattedDateTime(response.nearestShift[startAttr])]); 
        
                    } 
        
                } 
        
         
        
                return response; 
        
            }, 
        
         
        
            getNearestShift: function(upcomingShifts, startAttr, endAttr) { 
        
                if (gs.nil(upcomingShifts) || gs.nil(startAttr) || gs.nil(endAttr)) 
        
                    return; 
        
                var nearestShift; 
        
                upcomingShifts.sort(function(shift_1, shift_2) { 
        
                    var gdt1 = new GlideDateTime(); 
        
                    gdt1.setDisplayValueInternal(shift_1[startAttr]); 
        
                    var gdt2 = new GlideDateTime(); 
        
                    gdt2.setDisplayValueInternal(shift_2[startAttr]); 
        
                    return GlideDateTime.subtract(gdt2, gdt1).getNumericValue(); 
        
                }); 
        
                var currentDateTime = new GlideDateTime(), 
        
                    startDateTime = new GlideDateTime(), 
        
                    endDateTime = new GlideDateTime(); 
        
                for (var i = 0; i < upcomingShifts.length; i++) { 
        
                    startDateTime.setDisplayValueInternal(upcomingShifts[i][startAttr] + ""); 
        
                    endDateTime.setDisplayValueInternal(upcomingShifts[i][endAttr] + ""); 
        
                    if (currentDateTime.onOrBefore(endDateTime)) { 
        
                        nearestShift = upcomingShifts[i]; 
        
                        if (currentDateTime.onOrAfter(startDateTime)) 
        
                            nearestShift.isCurrent = true; 
        
                        else 
        
                            nearestShift.isCurrent = false; 
        
                        break; 
        
                    } 
        
                } 
        
                return nearestShift; 
        
            }, 
        
         
        
            getFormattedDateSpan: function(date, dateFormat, timeFormat) { 
        
                var formattedDate = this.getFormattedDate(date, dateFormat); 
        
                var dateAmPmTime = this.getFormattedTime(date, timeFormat); 
        
                return formattedDate + " " + dateAmPmTime; 
        
            }, 
        
         
        
            getFormattedDate: function(inputDate, format) { 
        
                var date = new GlideDateTime(); 
        
                date.setDisplayValueInternal(inputDate); 
        
                format = !format ? this.DATE_FORMAT : format; 
        
                var gd = date.getLocalDate(); 
        
                return gd.getByFormat(format); 
        
            }, 
        
         
        
            getFormattedTime: function(inputDate, format) { 
        
                var date = new GlideDateTime(); 
        
                date.setDisplayValueInternal(inputDate); 
        
                format = !format ? this.TIME_FORMAT : format; 
        
                var gt = date.getLocalTime(); 
        
                return gt.getByFormat(format); 
        
            }, 
        
         
        
            getFormattedDateTime: function(date) { 
        
                var dateTime = new GlideDateTime(); 
        
                dateTime.setDisplayValueInternal(date); 
        
                return dateTime.getDisplayValueLang(this.DATE_TIME_FORMAT_FULL); 
        
            }, 
        
         
        
            endsToday: function(inputDate) { 
        
                var inputGdt = new GlideDateTime(); 
        
                inputGdt.setDisplayValueInternal(inputDate); 
        
                return new GlideDateTime().getLocalDate().getValue() == inputGdt.getLocalDate().getValue(); 
        
            }, 
        
         
        
            endingTomorrow: function(inputDate) { 
        
                var inputGdt = new GlideDateTime(); 
        
                inputGdt.setDisplayValueInternal(inputDate); 
        
                var tomorrowDateTime = new GlideDateTime(); 
        
                tomorrowDateTime.addDaysLocalTime(1); 
        
                return tomorrowDateTime.getLocalDate().getValue() == inputGdt.getLocalDate().getValue(); 
        
            }, 
        ```

    4.  Edit the following part of the script as mentioned.

        ```
                    if (isOnCall) { 
        
                        if (response.nearestShift.isCurrent) { 
        
                            if (response.nearestShift.roster_name) 
        
                                response.shiftText = gs.getMessage("You are on-call until {0} as {1}", [this.getFormattedDateTime(response.nearestShift[endAttr]), response.nearestShift.roster_name]); 
        
                            else 
        
                                response.shiftText = gs.getMessage("You are on-call until {0}", [this.getFormattedDateTime(response.nearestShift[endAttr])]); 
        
                        } else { 
        
                            if (response.nearestShift.roster_name) 
        
                                response.shiftText = gs.getMessage("Your next on-call shift starts on {0} as {1}", [this.getFormattedDateTime(response.nearestShift[startAttr]), response.nearestShift.roster_name]); 
        
                            else 
        
                                response.shiftText = gs.getMessage("Your next on-call shift starts on {0}", [this.getFormattedDateTime(response.nearestShift[startAttr])]); 
        
                        } 
        
                    } else { 
        
                        if (response.nearestShift.isCurrent) { 
        
                            response.shiftText = gs.getMessage("Your shift ends on {0}", [this.getFormattedDateTime(response.nearestShift[endAttr])]); 
        
                        } else 
        
                            response.shiftText = gs.getMessage("Your next shift starts on {0}", [this.getFormattedDateTime(response.nearestShift[startAttr])]); 
        
                    } 
        ```

6.  Select **Update**.


