---
title: Methods of UI Automation mode and Active Accessibility mode
description: The Universal app connector provides multiple methods that perform various actions when screens are captured in Windows applications, for UI Automation mode and Active Accessibility mode.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-04-24"
reading_time_minutes: 1
breadcrumb: [Universal app connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Methods of UI Automation mode and Active Accessibility mode

The Universal app connector provides multiple methods that perform various actions when screens are captured in Windows applications, for UI Automation mode and Active Accessibility mode.

## Methods of UI Automation mode

If the screens are captured in Windows applications, for UI Automation mode, double-click the **UniversalApplication** object under Global Objects. The following methods for different element types appear in the Object Explorer pane.

|UI Automation Element Type|UI Automation Method Name|
|--------------------------|-------------------------|
|Common|Click|
|Common|Focus|
|Common|GetInstanceCount|
|Common|GetProperty|
|Common|IsCreated|
|Common|MouseAction|
|Common|ScrollIntoView|
|Common|SendKeys|
|Common|SetElementIndex|
|Common|SetLocatorValue|
|Common|SetLocatorValueArgs|
|Common|SetMatchRuleValue|
|Common|WaitForCreate|
|Edit|GetText|
|Edit|SetText|
|ComboBox|SetComboBoxItem|
|ComboBox|GetComboBoxItem|
|ComboBox|GetComboBoxItems|
|ComboBox|SelectNextItem|
|ComboBox|SelectFirstItem|
|ComboBox|ExpandComboBox|
|ComboBox|CollapseComboBox|
|Label|GetText|
|CheckBox|IsChecked|
|CheckBox|Check|
|CheckBox|UnCheck|
|Image|GetImage|
|ListBox|GetTable|
|ListBox|SelectListItem|
|ListBox|SelectNextItem|
|ListBox|SelectFirstItem|
|ListBox|SelectListItemByIndex|
|ListBox|ClickCell|
|ListItem|SelectItem|
|ListItem|AddToSelection|
|ListItem|IsSelected|
|Password|SetText|
|Password|GetText|
|Password|GetProperty|
|Password|SetPassword|
|RadioButton|IsChecked|
|RadioButton|Check|
|Table|GetTable|
|TreeView|ExpandAll|
|TreeView|CollapseAll|
|TreeView|SelectNextItem|
|TreeView|SelectFirstItem|
|TreeView|SelectItemByText|

## Methods of Active Accessibility mode

If the screens are captured in Windows applications, for Active Accessibility mode, double-click the **UniversalApplication** object under Global Objects. The following methods for Common element type appear in the Object Explorer pane.

|Element type|Active Accessibility Method Name|
|------------|--------------------------------|
|Common|DoDefaultAction|
|Common|SetValue|
|Common|GetValue|
|Common|Select|
|Common|Focus|
|Common|GetInstanceCount|
|Common|GetProperty|
|Common|IsCreated|
|Common|MouseAction|
|Common|SendKeys|
|Common|SetElementIndex|
|Common|SetLocatorValue|
|Common|SetLocatorValueArgs|
|Common|SetMatchRuleValue|
|Common|WaitForCreate|

**Parent Topic:**[Universal app connector](../concept/universal-app-connector.md)

