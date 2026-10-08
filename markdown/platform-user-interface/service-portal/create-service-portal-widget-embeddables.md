---
title: Create a Service Portal widget with embeddables
description: Create a Service Portal widget that displays an embeddable component. Add the component to the widget HTML and then call the embeddable APIs in a widget client script.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/service-portal/create-service-portal-widget-embeddables.html
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-09-25"
reading_time_minutes: 1
breadcrumb: [Embeddables in Service Portal, Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Create a Service Portal widget with embeddables

Create a Service Portal widget that displays an embeddable component. Add the component to the widget HTML and then call the embeddable APIs in a widget client script.

## Before you begin

Role required: admin

## Procedure

1.  In the widget HTML template file, add the embeddable component using its tag name.

    ```
    <case-list data-test-id="case-list" data-filter-config="$ctrl.filters"></case-list>
    ```

2.  Replace `case-list` with the tag name of your embeddable component.

3.  In your widget client controller, inject the `spEmbeddables` service.

    For example:

    ```
    app.controller('caseListWidget', function($scope, spEmbeddables) {
      // Widget logic here
    });
    ```

4.  Call the `getEmbeddables()` method to retrieve the component data by tag name.

    For example:

    ```
    app.controller('caseListWidget', function($scope, spEmbeddables) {
      spEmbeddables.getEmbeddables(['case-list']).then(function(components) {
        $scope.caseList = components['case-list'];
      });
    });
    ```

5.  Register event handlers.

    For example:

    ```
    $scope.setupEvents = function() {
      var caseListElement = document.querySelector('case-list');
      spEmbeddables.setEvents(caseListElement, {
        onSelect: $scope.onCaseSelect,
        onUpdate: $scope.onCaseUpdate
      });
    };
    
    $scope.onCaseSelect = function(caseId) {
      spUtil.addInfoMessage('Case ' + caseId + ' selected');
    };
    ```

6.  Use the `setProperties()` method to dynamically change component properties.

    For example:

    ```
    $scope.updateFilter = function(newFilter) {
      var caseListElement = document.querySelector('case-list');
      spEmbeddables.setProperties(caseListElement, {
        filterConfig: newFilter
      });
    };
    ```

7.  Add the widget to a Service Portal page.

    For more information, see [Create and edit a page using the Service Portal Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/service-portal/t_ConfigureAPage.md).

8.  Load the portal page in a browser and verify that the embeddable component displays and functions as expected.


## Result

Your Service Portal widget displays and interacts with the embeddable component.

**Parent Topic:**[Embeddables in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/service-portal/embeddables-service-portal.md)

