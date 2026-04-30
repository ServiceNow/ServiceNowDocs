---
title: Use OAuth to create pipeline credentials
description: Create credential records on each of your instances to enable OAuth use in your pipeline.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Configure OAuth credentials for use in Pipelines and Deployments, Configure environment credentials, Pipelines and Deployments configuration tasks, Configure Pipelines and Deployments, Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Use OAuth to create pipeline credentials

Create credential records on each of your instances to enable OAuth use in your pipeline.

## Before you begin

Complete the tasks in [Create OAuth API endpoints for external clients](create-oauth-api-endpoints-for-external-clients.md) and [Create third-party OAuth provider records](create-third-party-oauth-provider-records.md).

In the top right corner of your instance, make sure you set the application scope to **Global**.

Open all of your instances \(development, test, production, and the like\) in separate browser tabs.

Role required: admin

## About this task

To configure credentials correctly, you must create records for each of your production and non-production instances on your production instance. Then, you must create a record for your production instance on each of your non-production instances connecting them all together. Use the videos in each section to follow along with the steps. Begin on your production instance.

## Procedure

1.  On your production instance, navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    Create credential records on your production instance

2.  Select **New**.

3.  Change the **Type** to **Credential**.

4.  In the **Name** field, enter `Pipeline Dev OAuth`.

5.  Select **Submit**.

6.  Reopen the record you just created \(Pipeline Dev OAuth\).

7.  On the Credentials related list, select **New**.

8.  Select **OAuth 2.0 Credentials**.

9.  On the form, fill in the fields.

    |Field|Action|
    |-----|------|
    |Name|Enter `Dev OAuth`.|
    |OAuth Entity Profile|Search for and select the **Dev Instance Connection default profile**.|

10. Select **Submit**.

11. Reopen the **Dev OAuth** credential record.

    An expected error appears, directing you to verify the OAuth configuration and select **Get OAuth Token** to request a new token.

12. Under Related Links, select **Get OAuth Token**.

    A development instance opens requesting to connect to your ServiceNow account.

13. Select **Allow**.

14. Go back to the Connection &amp; Credential Aliases list \(**All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**\).

15. Select **New**.

16. Change the **Type** to **Credential**.

17. In the **Name** field, enter `Pipeline Test OAuth`.

18. Select **Submit**.

19. Reopen the record you just created \(Pipeline Test OAuth\).

20. On the Credentials related list, select **New**.

21. Select **OAuth 2.0 Credentials**.

22. On the form, fill in the fields.

    |Field|Action|
    |-----|------|
    |Name|Enter `Test OAuth`.|
    |OAuth Entity Profile|Search for and select the **Test Instance Connection default profile**.|

23. Select **Submit**.

24. Reopen the Test OAuth credential record.

    An expected error appears, directing you to verify the OAuth configuration and select **Get OAuth Token** to request a new token.

25. Under Related Links, select **Get OAuth Token**.

    A test instance opens requesting to connect to your ServiceNow account.

26. Select **Allow**.

27. Go back to the Connection &amp; Credential Aliases list \(**All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**\).

28. Select **New**.

29. Change the **Type** to **Credential**.

30. In the **Name** field, enter `Pipeline Prod OAuth`.

31. Select **Submit**.

32. Reopen the record you just created \(Pipeline Prod OAuth\).

33. On the Credentials related list, select **New**.

34. Select **OAuth 2.0 Credentials**.

35. On the form, fill in the fields.

    |Field|Action|
    |-----|------|
    |Name|Enter `Prod OAuth`.|
    |OAuth Entity Profile|Search for and select the **Prod Instance Connection default profile**.|

36. Select **Submit**.

37. Reopen the Prod OAuth credential record.

    An expected error appears, directing you to verify the OAuth configuration and select **Get OAuth Token** to request a new token.

38. Under Related Links, select **Get OAuth Token**.

    A production instance opens requesting to connect to your ServiceNow account.

39. Select **Allow**.

40. If you have any other non-production instances \(staging, etc.\), create a credential record for each of them on your production instance using the methods above.

    **Important:** After you've completed the steps above on your production instance, follow the steps below to create one credential record on each of your non-production instances connecting them to your production instance. Complete the next steps on your development instance.

41. On your development instance, navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    Create a credential record on your development instance and connect it to production.

42. Select **New** to create a record to connect your development instance to production.

43. Change the **Type** to **Credential**.

44. In the **Name** field, enter `Pipeline Prod OAuth`.

45. Select **Submit**.

46. Reopen the record you just created \(Pipeline Prod OAuth\).

47. On the Credentials related list, select **New**.

48. Select **OAuth 2.0 Credentials**.

49. On the form, fill in the fields.

    |Field|Action|
    |-----|------|
    |Name|Enter `Prod OAuth`.|
    |OAuth Entity Profile|Search for and select the **Prod Instance Connection default profile**.|

50. Select **Submit**.

51. Reopen the Prod OAuth credential record.

    An expected error appears, directing you to verify the OAuth configuration and select **Get OAuth Token** to request a new token.

52. Under Related Links, select **Get OAuth Token**.

    A production instance opens requesting to connect to your ServiceNow account.

53. Select **Allow**.

    **Important:** Complete the next steps on your test instance.

54. On your test instance, navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    Create a credential record on your test instance and connect it to production.

55. Select **New** to create a record to connect your test instance to production.

56. Change the **Type** to **Credential**.

57. In the **Name** field, enter `Pipeline Prod OAuth`.

58. Select **Submit**.

59. Reopen the record you just created \(Pipeline Prod OAuth\).

60. On the Credentials related list, select **New**.

61. Select **OAuth 2.0 Credentials**.

62. On the form, fill in the fields.

    |Field|Action|
    |-----|------|
    |Name|Enter `Prod OAuth`.|
    |OAuth Entity Profile|Search for and select the **Prod Instance Connection default profile**.|

63. Select **Submit**.

64. Reopen the Prod OAuth credential record.

    An expected error appears, directing you to verify the OAuth configuration and select **Get OAuth Token** to request a new token.

65. Under Related Links, select **Get OAuth Token**.

    A production instance opens requesting to connect to your ServiceNow account.

66. Select **Allow**.

67. If you have any other non-production instances \(staging, etc.\), create a credential record on that instance for production using steps 54-66.


## What to do next

Now that you've created all of the credential records connecting your instances, you can use those records to configure your pipeline environments. For more information, see [Configure your pipeline environments](config-pipeline-environments.md).

**Parent Topic:**[Configure OAuth credentials for use in Pipelines and Deployments](configure-oauth-credentials-pipelines-deployments.md)

