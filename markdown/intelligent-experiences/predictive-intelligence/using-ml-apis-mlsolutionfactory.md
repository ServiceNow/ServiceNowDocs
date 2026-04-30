---
title: Using MLSolutionFactory scriptable objects
description: MLSolutionFactory scriptable objects enable defining ML functionality. You can use the APIs to compose data-driven functionality, such as subclustering large clusters or clusters with multiple PRBs attached.
locale: en-US
release: zurich
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2026-03-27"
reading_time_minutes: 1
breadcrumb: [Using Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Using MLSolutionFactory scriptable objects

MLSolutionFactory scriptable objects enable defining ML functionality. You can use the APIs to compose data-driven functionality, such as subclustering large clusters or clusters with multiple PRBs attached.

You can use scriptable objects in a scripted extension point to modify the Predictive Intelligence REST API method to address unique business use cases.

ServiceNow applications on the NOW platform can call scriptable objects and script includes. External applications can call scripted REST APIs. By default, the Predictive Intelligence REST API - Prediction for multiple solutions \(GET\) method uses the MLSolutionUtil scripted extension point to take a list of active solution names, run predictions on them given the input, and return results. The MLSolutionUtil extension point enables creating custom implementations for specific usage scenarios, for example, running a second solution prediction only after the condition of a first solution prediction is satisfied.

Here's the high-level process for creating a custom usage scenario.

1.  Developers customize a MLSolutionUtil scripted extension point implementation using the MLSolutionFactory scriptable object.
    -   Listed as global.MLSolutionUtil in the Extension Point \[sys\_extension\_point\] table
    -   See [Register a custom script include](https://www.servicenow.com/docs/access?context=impl-client-ext-pts-base-code&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)
2.  The MLSolutionUtil scripted extension point implementation uses MLSolutionFactory to get the scriptable object, and invokes prediction methods on that object.
3.  The Predictive Intelligence REST API - Prediction for multiple solutions \(GET\) method invokes the MLSolutionUtil extension point implementation, depending on the scope of the request.
4.  Applications call the Predictive Intelligence REST API - Prediction for multiple solutions \(GET\) end point from a script include form.

For more information, see

-   [Predictive Intelligence REST API](https://www.servicenow.com/docs/access?context=agent-intelligence-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)
-   [MLSolutionFactory - Global](https://www.servicenow.com/docs/access?context=MLSolutionFactoryAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

