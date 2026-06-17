---
title: Mobile Onboarding for iOS v10.0.3
description: The iOS v10.0.3 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2020-06-01"
reading_time_minutes: 2
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for iOS v10.0.3

The iOS v10.0.3 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding/id1472486882). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_rbw_2jr_2jb"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile iOS \(non-classic\)

 PRB1406196

</td><td>

The dependency of the field on a UI parameter does not work unless the dependent field is also added as a UI parameter on the action screen

</td><td>

1.  Navigate to the instance and open the function named 'Reassign incident'.
2.  Remove the UI parameter for Assignment group and also remove the parameter mapping for the same so that Assignment group does not show up on the action screen.

This leaves Assigned to as the only parameter visible on the action screen.

3.  Add another UI parameter \(anything apart from Assigned to\) on the function so that Assigned to is not the only one.
4.  Open the applet Active incidents and use the swipe function Reassign on a record that already has an assignment group on it.
5.  Tap on the **Assigned to** field.

 Expected behavior: The user records associated with the Assignment group should show up since Assigned to is a dependent field of Assignment group.

 Actual behavior: When Assignment group is not added as a UI parameter on the action screen, all user records show up, and the dependency is not honored.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1406059

</td><td>

When Search List is added as a UI parameter, navigating to the parameter and then cancelling is removing the value on the action screen

</td><td>

1.  Navigate to the instance and open the function named 'Reassign incident'.
2.  Navigate to the UI parameter for Assignment group and change the input type to Search List.
3.  Save the record.
4.  Open the applet Active incidents and use the swipe function Reassign on a record that already has an assignment group on it.
5.  On the action screen, observe the two parameters, **Assignment Group** and **Assigned To**.

Notice that **Assignment Group** has a value in it.

6.  Tap on **Assignment Group**.

The list of groups shows up.

7.  Cancel this screen without any new selection.

 Expected behavior: Since no selection is made, it should retain the prior value.

 Actual behavior: Previously stored value for Assignment Group on the action screen is gone.

</td></tr></tbody>
</table>This version also includes other minor bug fixes.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

