---
title: Use Now Assist for Supplier Lifecycle Operations \(SLO\) in a Virtual Agent chat
description: Use the conversational interface of Now Assist for Supplier Lifecycle Operations \(SLO\) to request contextually relevant generative AI capabilities through a Virtual Agent chat.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
keywords: [generative AI, gen AI, genai, artificial intelligence]
breadcrumb: [Use Now Assist for Supplier Lifecycle Operations \(SLO\), Now Assist for Supplier Lifecycle Operations \(SLO\), Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Use Now Assist for Supplier Lifecycle Operations \(SLO\) in a Virtual Agent chat

Use the conversational interface of Now Assist for Supplier Lifecycle Operations \(SLO\) to request contextually relevant generative AI capabilities through a Virtual Agent chat.

Role required: sn\_supplier\_gen\_ai.now\_assist\_supplier

**Note:** This role must be provided to the sn\_slm.contact user.

As a supplier, you can use the predefined topics \(chatbot conversations\) that are designed to help you complete self-service tasks. You can manage a profile, manage users, submit a request, track request status, or connect to a live agent by using contextual generative AI capabilities.

To start a conversation, navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Supplier Collaboration Portal** and select the Virtual Agent chat icon \(![Chat icon.](../image/open-chat-window-icon.png)\).

The following example shows the starting screen for the Now Assist for SLO in a Virtual Agent chat.

![Show all my options.](../image/now-assist-slo-va-start.png "Starting screen for the Now Assist for SLO in a Virtual Agent chat")

Then, you select **Show all my options** as shown in the following example.

![All topics.](../image/now-assist-slo-all-topics.png "All topics in the Now Assist for SLO in a Virtual Agent chat")

## Using a predefined topic to update the bank details

As a supplier contact, you can update your existing bank details or submit a new one by selecting **Show all my options** &gt; **Update banking details**. You could also directly start entering the instructions.

You must enter the email address that is associated with your organization's account to update your bank details. Follow the instructions in the chat to complete the procedure as shown in the following example.

![Summary of your bank details.](../image/now-assist-slo-update-bank.png "Update the bank details")

You must upload proof of the beneficiary's bank account to edit the request.

Select **Yes, submit** to create a supplier case.

## Using a predefined topic to update the location details

As a supplier contact, you can add a new location or remove an existing one by selecting **Show all my options** &gt; **Update location details**. You could also directly start entering the instructions.

For example, enter `Add new location details` in the chat to add a new location. Select a country from the list and follow the prompts in the chat to complete the procedure as shown in the following example.

![Summary of the updated location.](../image/now-assist-slo-location.png "Update the location details")

Select **Yes, submit** to create a supplier case.

## Using a predefined topic to update the profile details

As a supplier contact, you can update the profile details by selecting **Show all my options** &gt; **Update profile details**. You could also directly start entering the instructions.

Select **Edit request** to update the profile details and enter the profile details that you want to update. Follow the prompts in the chat to complete the procedure.

Select **Yes, submit** to create a supplier case as shown in the following example.

![Supplier case created for the profile update request.](../image/now-assist-slo-profile.png "Supplier case for the profile update")

## Using a predefined topic to submit a request

As a supplier contact, you can submit a request by selecting **Show all my options** &gt; **Submit a request**. You could also directly start entering the instructions.

Enter `Supplier inquiry` in the chat, describe the case, and select a supplier contact from the list to create a request as shown in the following example.

![Summary of the new request created.](../image/now-assist-slo-request.png "Submit a request")

Select **Yes, submit** to create a supplier case.

## Using a predefined topic to track a request status

As a supplier contact, you can track a request status by selecting **Show all my options** &gt; **Track request status**. You could also directly start entering the instructions.

For example, enter `I want to know the status of SCASE0001156` in the chat to view the status of the request as shown in the following example.

![Summary of the supplier case.](../image/now-assist-slo-track-request.png "Track a request status")

## Using a predefined topic to enroll a new user

As a supplier contact, you can enroll a new user by selecting **Show all my options** &gt; **Enroll a new user**. You could also directly start entering the instructions.

Enter the work email address of the new user and select if you want this new user as the primary contact as shown in the following example.

![Summary of the request to enroll a new user.](../image/now-assist-slo-new-user.png "Enroll a new user")

Select **Yes, submit** to create a supplier case.

## Using a predefined topic to remove a user account

As a supplier contact, you can remove a user account by selecting **Show all my options** &gt; **Remove user account**. You could also directly start entering the instructions.

Enter the name of the user or the email address of the user account that you want to remove. Enter the email address of the user who will take over the tasks that were delegated to the removed user. You must also provide a reason for offboarding this user. The following example shows how to remove a user account.

![Summary of the request to remove a user account.](../image/now-assist-slo-remove-user.png "Remove a user account")

Select **Yes, submit** to create a supplier case.

## Using a predefined topic to request an access change

As a supplier contact, you can request an access change by selecting **Show all my options** &gt; **Request access change**. You could also directly start entering the instructions.

**Note:** Only a secondary contact can request an access change.

Select the urgency of the access change, such as low, moderate, or high. Enter the reason for requesting the access change from secondary to primary as shown in the following example.

![Summary of the request for an access change.](../image/now-assist-slo-access-change.png "Request an access change")

Select **Yes, submit** to create a supplier case.

## Using a predefined topic to connect to a live agent

As a supplier contact, you can connect to a live agent by selecting **Show all my options** &gt; **Connect to a live agent**.

Select **Supplier management team** to connect to a live agent as shown in the following example.

![Agent available to help you.](../image/now-assist-slo-live-agent.png "Connect to a live agent")

## Additional Information

Now Assist in Virtual Agent provides your users with an interactive generative AI experience. A friendly, natural language conversation is easier to understand and makes supplier contacts more comfortable with talking to a bot. To learn how a conversation that is powered by generative AI might look in Virtual Agent, see [Using Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

As an administrator, you can use the Now Assist in Virtual Agent Analytics dashboard to monitor the performance of Now Assist in Virtual Agent as a self-service deflection tool. To learn more, see . Now Assist in Virtual Agent Analytics calculates the conversation deflection rate that is based on the resolution status associated with Now Assist query responses. For more information, see .

For detailed information on Now Assist in Virtual Agent in general, and Now Assist for SLO in particular, see [Explore Now Assist for Supplier Lifecycle Operations \(SLO\)](now-assist-slo-exploring.md).

For information on configuring Now Assist for SLO, see [Configure Now Assist for Supplier Lifecycle Operations \(SLO\)](../task/now-assist-slo-configuring.md).

