---
title: View SRM reliability metrics
description: View a service level objective \(SLO\) and service level indicator \(SLI\) that your or your team owns.
locale: en-US
release: yokohama
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Using SLO Management, Service Level Objective Management, ITOM AIOps, IT Operations Management]
---

# View SRM reliability metrics

View a service level objective \(SLO\) and service level indicator \(SLI\) that your or your team owns.

## Before you begin

Role required: Responder, Manager, or Administrator

**Note:** Administrators can view any SRM SLO.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You're taken to your SRM Home page.

    **Note:** If you use other Service Operations Workspace \(SOW\) applications, you may see the SOW Home page instead of the SRM Home page. The SOW Home page includes SRM alerts and incidents in its metrics.

2.  From the primary navigation, select the **Services** icon \(![Services icon](../image/icon-sr-services.png)\).

3.  Select the **Reliability metrics** tab.

4.  Open a **Service level objective**.

5.  View the SLO header.

    The top header contains service information for:

    -   **SLI type**:

        Type of the SLI based on which the metrics are calculated. The available types of SLI are as follows:

        -   **Availability**: Percentage of time your service is available. \(Default\)
        -   **Errors**: Measurement of how frequently service error occurs.
        -   **Latency**: Time taken to service a request. The actual amount of time that elapsed.
        -   **Saturation**: Measurement of your system fraction, emphasizing the resources that are most constrained.
        .

    -   **SLO Type**:

        Type of SLO based on which metric you choose. The available types of SLO are as follows:

        -   **Duration**: The amount of time the service spends without breaching. It’s the only value available.

            Metrics for **Duration** are as follows:

            -   **Objective \(percentage\)**: Percentage of the desired SLI performance.
            -   **Error budget**: Displays, in days and time, how much error budget is left.
        -   **Count**: Number of occurrences in a given compliance period.

            Metrics for **Count** are as follows:

            -   **Limit \(occurrences\)**: Number of occurrences after which a breach has occurred.
            -   **Remaining breach occurrences**: Number of occurrences left.
    -   **State**:

        State of the SLO. Choices are:

        -   Draft: The SLO isn't running in your instance yet. You can add new SLIs or update existing SLIs and you can delete the SLO.
        -   Running: The SLO is active in your instance. You can edit, retire, or delete the SLO.

            **Note:** Editing an SLO in the running state retires it and a new copy is created.

        -   Retired: The SLO is no longer running in your instance. You can reactivate it.
    -   **Service**: Service associated with the SLO.
    -   **Reliability**: How reliable the service is.

        -   **Stable**: All SLOs in this Service have more than 25% of the error budget still available.
        -   **At RISK**: All SLOs in this Service Have EB left, and at least one SLO for this Service has less than 25% of the error budget left.
        -   **Critical**: Any one SLOs in this Service has burnt through its error budget
    From the header you can **Delete SLO**, **Retire**, or **Edit**.

    If you delete an SLO any associated SLIs are deleted as well.

    If you retire an SLO, it changes the state. You can **Re-activate** it from the SLO page or later from the **Reliability metrics** tab.

    **Note:** If you edit an SLO, it changes the state, retires the SLO record, and opens a new copy for editing. See [Create SLOs, SLIs, and error budget policies](../../slo-management/task/sr-create-slo-sli.md) for more information. You can reactivate the original SLO by returning to the **Reliability metrics** tab.

6.  View the **Overview** tab and select a Historic period from the list menu.

    The periods listed are from the date that the SLO was created to the present in the selected increments.

7.  View **Summary** metric cards for the SLO.

    The metrics show aggregate or average values depending on the type of SLIs chosen and error policy thresholds chosen. See [Create SLOs, SLIs, and error budget policies](../../slo-management/task/sr-create-slo-sli.md) for more detailed information.

8.  View the **Service level indicators** section.

    This section lists your indicators by name.

9.  View the **Service level objective \(SLO\) history** section.

    Depending on your **SLO type**, this section displays the following in bar graph reports:

    For **Duration**:

    -   Error budget used
    -   Error budget remaining
    -   Burn rate
    For **Count**, **Count by periods**, or **Count by occurrences**:

    -   Cumulative breach occurrences
    -   Burn rate
    -   Alerts, incidents &amp; changes impacting this service
    Selecting into one of the analytics line chart reports shows the values on that day.

10. View the **Details** tab.

    The fields in this tab are auto-populated and uneditable. See [Create SLOs, SLIs, and error budget policies](../../slo-management/task/sr-create-slo-sli.md) for detailed information on the fields.

11. View the **Service level indicators** tab.

    This tab lists the SLIs associated with this SLO.

12. View the **Error budget policy** tab.

    In this tab, you can add more thresholds and edit or delete existing ones.

    ![Error budget policy page.](../image/sr-slo-error-budget-policy.png)


**Parent Topic:**[Using SLO Management](../../slo-management/task/using-service-level-objective-management.md)

