---
title: Reserve a space using ServiceNow Otto for Virtual Agent
description: The Reserve a space virtual agent enables you to create a reservation using ServiceNow Otto for Workplace Service Delivery \(WSD\). You can also add services to your reservation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/now-assist-for-wsd/wsd-reserve-a-space-now-assist-va.html
release: zurich
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: task
last_updated: "2026-07-28"
reading_time_minutes: 9
breadcrumb: [Using ServiceNow Otto for WSD, ServiceNow Otto for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Reserve a space using ServiceNow Otto for Virtual Agent

The Reserve a space virtual agent enables you to create a reservation using ServiceNow Otto for Workplace Service Delivery \(WSD\). You can also add services to your reservation.

## Before you begin

The **Reserve Space** topic should be added to ServiceNow Otto for Virtual Agent. For more information, see [Configure ServiceNow Otto for Virtual Agent for Workplace Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-wsd/config-now-assist-va-wsd.md).

Make sure that you have the following applications:

-   ServiceNow Otto for Platform \(sn\_genai\_platform\)
-   Workplace Reservation Management Workplace Reservation Management \(sn\_wsd\_rsv\)

Role required: sn\_wsd\_core.workplace\_user

## Procedure

1.  Log in to the Employee Center portal.

    For more information, see [Workplace services on the Employee Center portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-core/workplace-services-on-employee-center.md).

2.  Select and open the chat window.

3.  Enter your query or key words to reserve a meeting room.

    The bot supports human-like conversational language. For example, you can query ' 'Reserve a space for me', I want to reserve a space for 10 AM, and so on.

4.  After the initial greeting message, the bot provides an explanation of what you can expect from it.

5.  Enter your query or key words to reserve a space.

    A friendly, natural language conversation or utterance can be used while making or submitting your workplace requests.

    While the large language model \(LLM\) is processing your request \(utterance\), animated dots in the chat window indicate that the bot is working on your request.

6.  The ServiceNow Otto for Virtual Agent shows options to reserve a space.

    \[Omitted image "wsd-reserve-a-space-topic-nowassist.png"\] Alt text: ServiceNow Otto for Virtual Agent showing the Reserve space topic.

    **Note:** The option to reserve a space using the ServiceNow Otto for Virtual Agent is available only if your administrator has added the **Reserve Space** Virtual Agent LLM topic in the Virtual Agent designer. For more information, see [Configure ServiceNow Otto for Virtual Agent for Workplace Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-wsd/config-now-assist-va-wsd.md).

7.  Select **\(Topic\) Reserve Space**.

    When the Topic name button is selected, the workplace requester is launched into that topic flow within the ServiceNow Otto for Virtual Agent.

    The application tries to find “keywords” in the sentences that the employee enters. It uses the keywords entered by an employee for reservation requests and shows suggestions for reserving a space step by step. Based on the input provided, the bot tries to get as many data points as possible initially. For example; “I want to reserve a desk for Friday from 9 am till 11 am” are the keywords entered by an employee. The application captures the following data points and shows suggestions:

    -   Space type: the system will filter on modules with "space" in it
    -   Building AMS-B1, the employee is asked to confirm
    -   Start time: 9 am
    -   End time: 11 am
    Since, there is no date provided, the employee is asked by the bot to indicate the date.

    For example, if the employee enters "I want a space on next Monday from 9 am to 11 am," the building information is not provided. The bot asks the employee to indicate the building. The date is calculated using the input "Next Monday" and start and end time. The more information an employee provides, the fewer inputs the bot requires to process and create a reservation.

8.  The ServiceNow Otto for Virtual Agent bot instructs you to select the type of reservation that you want to make.

    For example, select **Meeting rooms.**

    **Note:** Only the **Browse All** Reservable module configuration is supported by Now Virtual Agent. It shows all reservation types available in the **Browse All** Reservable module. For example, **Desks**, **Desks within a shift**, and so on.

    The **Specific Unit** **Selection type** is supported in the Reservable Table configuration. **Container** isn’t supported for ServiceNow Otto for Virtual Agent. For more information, see [Configure a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-reservation-management/config-reservable-module.md).

9.  The ServiceNow Otto for Virtual Agent bot instructs you to select a location for reserving a space.

10. Select a building.

    For example, **Cal-B2**.

    \[Omitted image "wsd-locations-now-assist.png"\] Alt text: ServiceNow Otto for Virtual Agent showing location names.

11. ServiceNow Otto for Virtual Agent bot instructs you to provide the Start and End dates for the reservation.

    **Note:** Recurring reservation and multi-day reservations are currently not available when you book a meeting room using the bot. Only single reservations for a selected date can be created. Make sure that the Start and end dates should be in the building's time zone and can’t be in the past.

12. ServiceNow Otto for Virtual Agent bot confirms your selection for a location and reservation dates.

13. ServiceNow Otto for Virtual Agent bot instructs you to provide the floor name, capacity, and space name where you want to reserve a meeting room.

    \[Omitted image "wsd-floor-reservation-summary-nowassist.png"\] Alt text: Now Assist in Virtual Agent prompts for adding a floor name.

    **Note:** Floor, capacity, and shift schedule are optional inputs. If there are no spaces available, the ServiceNow Otto for Virtual Agent bot shows the following message, "Sorry, there are no available spaces currently. Revise your selections and retry". If the suggestions don't match your requirement, you’re also given the option to select **None match my preference**. If invalid user inputs are provided, for example, an incorrect building name or a past date, the bot asks you to enter the details again.

    The ServiceNow Otto for Virtual Agent bot shows location results. The name of the building, floor, and capacity are displayed in the result.

    \[Omitted image "wsd-floor-reservation-summary-nowassist.png"\] Alt text: Provide the capacity of the floor.

    \[Omitted image "wsd-capacity-floor-nowassist.png"\] Alt text: ServiceNow Otto for Virtual Agent showing the space name and capacity.

    Select a space from the suggestions showed by ServiceNow Otto for Virtual Agent.

    The ServiceNow Otto for Virtual Agent processes the information that you have provided and completes your reservation.

14. To view and update the reservation details, select the link **Click here to view reservation details.**

    The Reservation summary page appears. On the Reservation summary page, you can edit and update your reservation details.

15. ServiceNow Otto for Virtual Agent provides suggestions to add services to your reservation.

    You can add guests and external visitors, Zoom virtual meeting link, or Catering services to your reservation. If you don’t want to add any of these services to your reservation, you can skip this step and complete your reservation at this stage.

    **Note:** The option to add workplace services is shown based on the corresponding service availability for a selected location. For example, if Zoom spoke and the virtual meeting provider is configured in the Reservable module, the Added Zoom service option is shown by the bot. This also depends on the availability of a location or reservable module configuration settings by your administrator. So, if there is no Zoom spoke configured or guests aren't allowed to a reservation, the bot doesn't display the related questions or suggestions. For catering services, the application checks if these are assigned for a selected location.

16. ServiceNow Otto for Virtual Agent instructs you to invite guests to your reservation.

    **Note:** The option to add guests is shown only when the **Allow Invitees** configuration is enabled in the Reservation module. This option in the Reservable Module enables you to invite attendees and add them to your reservation. You can invite guests to your reservation. For more information, see [Configure a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-reservation-management/config-reservable-module.md).

17. Select **Yes** if you want to add guests to your reservation.

    **Note:** You can add multiple invitees to your reservation. For more information, see [Configure ServiceNow Otto for Virtual Agent for Workplace Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-wsd/config-now-assist-va-wsd.md). You also need Workplace Visitor Management.

18. ServiceNow Otto for Virtual Agent provides suggestions to select your guests.

19. ServiceNow Otto for Virtual Agent confirms the guests details that you have provided.

20. Select **Yes** to proceed.

    Select **No** to change or update your selection.

21. After adding guests, you can add additional services like external visitors to your reservation.

    You can only add visitors to a reservation for which you're the host. Workplace users with 'sn\_wsd\_rsv.manager' or 'sn\_wsd\_rsv.reservation\_planner' roles can add invitees to a reservation. Workplace users with 'sn\_wsd\_core.workplace\_user' role can’t add invitees to a reservation when they aren't the host.

    \[Omitted image "wsd-visitor-email-id.png"\] Alt text: Visitor Email Id provided by Employee in the Virtual Agent.

    **Note:** Multiple visitors can’t be added all at once. You should add visitors sequentially. For example, if you have visitor A, visitor B, and visitor C. Start by adding visitor A first, and add visitor B, and Visitor C.

    1.  ServiceNow Otto for Virtual Agent instructs you to provide the First Name, Last Name, and Email ID of the external visitor.

        If a visitor that is already added to a reservation is added again, the bot provides suggestions to add another visitor.

    2.  Provide the required details.

    3.  After adding the visitor, ServiceNow Otto for Virtual Agent confirms that visitor registration is done.

    4.  Now Virtual Agent provides suggestions to add a few more visitors to your reservation.

    5.  You can select **Skip** to proceed and continue with your reservation.

22. ServiceNow Otto for Virtual Agent shows the option to Add Catering services.

    **Note:** The services that you add are default catering workplace services provided with Workplace Reservation Management. It doesn't support any custom catering or workplace services added by you.

    1.  Select the required catering services \(Lunch, Snacks, Drinks\).

        You can also enter or add a conversational text like "Add lunch, some snacks, and drinks", "Add sparkling water and some snacks, and so on".

        \[Omitted image "wsd-add-catering-options-now-assist.png"\] Alt text: ServiceNow Otto for Virtual Agent showing the catering services menu options.

        **Note:** When the requested catering service aren’t available, a message is shown that the requested catering service isn’t available.

    2.  The bot asks you to specify the quantity for all the selected catering menu items.

    3.  After confirming your selection, the bot adds the catering services to your reservation.

        \[Omitted image "wsd-add-catering-still-water-use-nowassist.png"\] Alt text: ServiceNow Otto for Virtual Agent asks to specify the quantity for selected catering services.\[Omitted image "wsd-add-catering-confirmation-message-now-assist.png"\] Alt text: ServiceNow Otto for Virtual Agent displaying the Catering services that are added to a reservation.

23. ServiceNow Otto for Virtual Agent provides prompts to add a zoom meeting link.

    Make sure that you have the following:

    1.  For more information, see [Configure ServiceNow Otto for Virtual Agent for Workplace Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-wsd/config-now-assist-va-wsd.md).
    2.  Zoom Spoke is configured for Workplace Reservation Management. For more information, see [Connect Workplace Reservation Management with Zoom](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-reservation-management/connect-rsv-mtm-with-zoom.md).
24. ServiceNow Otto for Virtual Agent shows an acknowledgment message along with the Workplace case task created after adding the Zoom virtual meeting link.

    \[Omitted image "wsd-add-zoom-meeting-2-nowassist.png"\] Alt text: ServiceNow Otto for Virtual Agent acknowledges adding the virtual meeting link to your reservation along with the Workplace Case task created for this request.

25. The ServiceNow Otto for Virtual Agent shows the reservation summary.

    \[Omitted image "wsd-now-assist-reservation-summary-final.png"\] Alt text: ServiceNow Otto for Virtual Agent summarizes the reservation details along with services that you have added to your reservation.


