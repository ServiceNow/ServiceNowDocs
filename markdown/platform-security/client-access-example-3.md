---
title: Create a secret group with criteria
description: Create a group for your secrets. Secret groups to organize your secrets into groups, and enable you to apply access policies to those secrets at a group level. Then associate your secrets group to an identity group, and add your MID Server to that identity group.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring client accessible secrets, Secrets Management, Platform Security]
---

# Create a secret group with criteria

Create a group for your secrets. Secret groups to organize your secrets into groups, and enable you to apply access policies to those secrets at a group level. Then associate your secrets group to an identity group, and add your MID Server to that identity group.

## Before you begin

Role required: admin, sn\_kmf.admin, sn\_secrets.admin

## Procedure

1.  Navigate to **All** &gt; **Secrets Management** &gt; **Secret Groups with Criteria**.

2.  Select **New** to create a **Secret Group with Criteria** record.

3.  In the form, fill in the following fields.

    |Field|Value|
    |-----|-----|
    |Group name|Name of the secret group. This name can be any name you choose.|
    |Secret type|Select **Client accessible**|
    |Autogen module|Check the box|
    |Short description|Description of the secret group. Enter a value that indicates what this group is being used for.|
    |Criterion type|Select **Target table**|
    |Target table|Select **SSH Credentials \[ssh\_credentials\]**|

4.  Select and hold \(or right-click\) the form header and select **Save** from the context menu to save the record.

5.  Make sure that the **Active** check box isn't checked.

6.  Select the **Manage client side access** button to create an identity group.

    An **Identity group alias** window displays.

7.  Select the **New** button.

8.  Select the reference icon \(![reference button](../images/magnifying_glass.png)\) next to the **Identity group alias** field.

9.  In the **Group Alias Name** field, enter a value.

    This name can be any value you want.

10. If you chose a unique name in Step 9, select **Submit**.

11. Select the **Upload identity key** button.

    The **Import identity public key certificate** window displays.

12. In the **Identity key alias** field, enter a value.

    **Important:** This value can be anything you want, but it must be an exact match for what you insert into the MID Server in later steps.

13. Select **Import**

    The **Attachment** window displays.

14. Select **Choose file**.

15. Select the public certificate that you created in the earlier steps.

    This certificate should be the `sm_public_cert.pem` file.

16. Select the X icon to close the window.

17. Select **OK** to close the **Import identity public key certificate** window.

    A blue **Keys and certificates are successfully imported to the instance** banner displays confirming a successful import.

18. Select **Submit**.

    The **Identity groups** list displays.

19. Select the check box to the left of your identity group record in the list.

20. Select the **Associate secret group** button.

    You're returned to your **Secret Group with Criteria** record. The **Secret Group – Identity Group Alias**” and **Secret Group – Identity Group** related lists are visible. These related lists display the records that you created in the previous steps.

21. In the **Secret Group – Identity Group** related list, select the **Created** field for the record on that list.

    ![Created field in the Secret Group – Identity Group related list](../images/client-side-4.png)

    An **Identity group** record displays.

22. In the **Identity group members** related list, select the **New** button.

    A **Identity group member** record displays.

23. In the **Member table** field, select **MID Server \[ecc\_agent\]**.

24. Select the reference icon \(![reference button](../images/magnifying_glass.png)\) next to the **Identity group member record** field, and select your MID Server.

    **Note:** If you enable the **Include all records** check box, all MID Servers connected to your instance are added to the identity group.

25. Select **OK** to close the **Select the document** window.

26. Select **Submit**.

27. Navigate back to **All** &gt; **Secrets Management** &gt; **Secret Groups with Criteria**, and open the record you created in step 2.

28. Enable the **Active** field.

29. Select **Update** to save the record.


**Parent Topic:**[Configuring client accessible secrets](../concept/client-access-secret-landing.md)

