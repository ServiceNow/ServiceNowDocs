---
title: Security Incident Response playbook actions
description: This section describes the actions provided in the Flow Designer action library.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response playbook actions

This section describes the actions provided in the Flow Designer action library.

<table id="table_pyf_3yn_pkb"><thead><tr><th>

Action Name

</th><th>

Description

</th><th>

Example scenario

</th><th>

 

</th></tr></thead><tbody><tr><td>

Add a security tag to the security incident

</td><td>

Use this action to add a security tag automatically using flow designer logic.

</td><td>

If the flow detects an IOC, the **IOC Detected** tag can be automatically added using this action.**Flow**:

</td><td>

-   Input: security incident, security tag
-   Output: not applicable

</td></tr><tr><td>

Add observables to the security incident

</td><td>

Use this action to add observables to a selected security incident. -   By default, the list of observables are separated by the comma \(,\) delimiter but this can be modified. You can specify another single special character as a delimiter. While adding observables, the type \(URL, IP address, hash\) is automatically set.
-   When the observables are added to the security incident, the type \(URL, IP address, hash\) is automatically set.
-   When the observables are being added, the Filter Allowed list Observables option identifies allowed list observables and does not add them to the security incident's observables related list. An automated system activity \(response\) is added to indicate that these observables have been removed.

</td><td>

 

</td><td>

-   Input:
    -   security incident
    -   observables
    -   delimiter
    -   filter allowed list observables and post activity note
-   Output: not applicable

</td></tr><tr><td>

Get affected users \(Related Lists\) from multiple security incidents V1

</td><td>

Retrieves all the affected users listed in the Affected Users related list for the specified security incidents.

</td><td>

You may have parent security incidents with multiple child security incidents. Use this action to roll-up affected users from all the child security incidents to the corresponding parent security incidents. Only unique affected users are rolled-up and all duplicates are eliminated.

</td><td>

-   Input: security incidents
-   Output:
    -   affected user
    -   count

</td></tr><tr><td>

Get affected users from multiple security incidents

</td><td>

Retrieves the primary affected user for the specified security incident. It does not include the affected users from the Affected User related list.

</td><td>

-   While investigating a phishing security incident, send an email to the primary affected users \(who reported the phishing incident\) to confirm if any of the users clicked on the malicious links in the phishing email.
-   Update the parent security incident severity or risk score based on the count of primary affected users.

</td><td>

-   Input: security incidents
-   Output:
    -   affected users
    -   count

</td></tr><tr><td>

Get affected users \(related list\) from a security incident

</td><td>

Retrieves all the affected users listed in the Affected Users related list for a specified security incident.

</td><td>

 

</td><td>

-   Input: security incidents
-   Output:
    -   affected users
    -   count

</td></tr><tr><td>

Add affected users to security incident

</td><td>

Adds all affected users to a security incident.

</td><td>

Suppose you have a parent security incident with multiple child security incidents. You can use this action to roll-up affected users from all the child security incidents to the corresponding parent security incident. Only unique affected users are rolled-up and all duplicates are eliminated.

</td><td>

-   Input:
    -   security incident
    -   user
-   Output: not applicable

</td></tr><tr><td>

Get configuration items of the affected users

</td><td>

Retrieves the configuration items \(CIs\) of all affected users.

</td><td>

In phishing or malware scenarios, you can use this action to update the Affected Configuration Items \(CI\) related list and investigate the CIs. You can then update the severity or risk score of the security incident based on the number of identified CIs.

</td><td>

-   Input: users
-   Output:
    -   configuration items
    -   count

</td></tr><tr><td>

Get all child security incidents for a security incident

</td><td>

Retrieves all child security incidents related to a specific parent security incident.

</td><td>

Example scenario: Use this action to:-   Update the status of the child security incidents when their corresponding parent security incidents status get updated.
-   Update the severity or risk score of the security incident automatically based on the number of child security incidents.

</td><td>

-   Input:
    -   security incident
    -   incident state
-   Output:
    -   child security incident
    -   count

</td></tr><tr><td>

Get configuration items for the observables \(type IP address\)

</td><td>

Retrieves all configuration items \(CIs\) for observables of type IP address.

</td><td>

An IP address observable can be associated with a configuration item. For example, the IP address of a server. If you use this action, you can retrieve information for the server.

</td><td>

-   Input: observable ip address
-   Output:
    -   configuration items
    -   count

</td></tr><tr><td>

Is observable malicious

</td><td>

Confirms the presence of one or more malicious observables in a set of observables.

</td><td>

After the threat lookup has been completed and you have identified the presence of malicious observables, you can increase the severity or risk score of a security incident.

</td><td>

-   Input: security incident
-   Output: malicious \(true/false\)

</td></tr><tr><td>

Send email to confirm user interaction

</td><td>

Sends email in response to a user response.

</td><td>

If a user tries multiple times to login to an application and fails, it results in a failed login scenario. In this case, an email is sent to the user to confirm whether the user attempted to login or not. Depending on the user response \(Yes or No\), different actions can be taken.**Flow**: Failed Login Manual playbook

</td><td>

 

</td></tr><tr><td>

Filter out allowed list observables

</td><td>

Use this action to allow list observables from a given set of observables.

</td><td>

You can identify certain observables that can be ignored from a set of observables. These observables will not taken into account while resolving the security incident.

</td><td>

-   Input: security incident
-   Output:
    -   allowed list observables
    -   count

</td></tr><tr><td>

Reset password for affected users

</td><td>

Use this action to reset password for affected users.

</td><td>

If a user account has been hacked or a user requests a password to be reset, an email is sent to the user to reset the password.**Flow**: Failed Login Manual playbook.

</td><td>

 

</td></tr><tr><td>

Get user group for affected user

</td><td>

Retrieves the user group details of affected users.

</td><td>

In an organization, if two or more users report phishing emails, you can find out the group they belong to and identify if more users have been affected

</td><td>

-   Input: user
-   Output:
    -   user groups
    -   count

</td></tr></tbody>
</table>