---
title: Pulling changes
description: Developers synchronize their instances to the parent instance by pulling and pushing versions of customized records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/team-development/c\_PullsAndPushes.html
release: zurich
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with changes, Team Development, Planning your application, Building applications]
---

# Pulling changes

Developers synchronize their instances to the parent instance by pulling and pushing versions of customized records.

Pulling retrieves all versions that haven’t already been pulled onto the development instance, including historical versions that have customer updates. You must resolve any collisions before proceeding with further pulls or pushes.

**Note:** You can’t choose specific versions to pull.

Comparing reports the differences between two peer instances. You can choose which versions to pull from a peer instance. You can learn about comparing instances [Compare to peer instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/t_CompareToAPeerInstance.md).

-   You can learn about pulling a version [Pull a version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/t_PullAVersion.md).

    Pulling retrieves versions of customized records from the parent instance and adds them on the development instance.

-   You can learn about the pull exceptions here [Pull exceptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/r_PullExceptions.md).

    Pulling ignores versions when certain conditions occur.


The pushes and pulls related list on the [Team dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/r_TeamDashboard.md) displays the user who created a change and the remote instance where the change was created.

-   **[Pull a version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/t_PullAVersion.md)**  
Pulling retrieves versions of customized records from the parent instance and adds them on the development instance. Pulling doesn’t retrieve any versions for changes made by system upgrades.

**Parent Topic:**[Local changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/c_LocalChanges.md)

