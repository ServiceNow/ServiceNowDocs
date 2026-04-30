---
title: Extend functionality of the Workday HR spoke
description: Extend the Workday HR spoke beyond the default functionalities, such as adding new input and output fields.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Extend functionality of the Workday HR spoke

Extend the Workday HR spoke beyond the default functionalities, such as adding new input and output fields.

To extend the Workday HR spoke, ensure that the admin is aware of the [Workday Public Web Services API](https://community.workday.com/sites/default/files/file-hosting/productionapi/versions/v33.2/index.html) and can configure the Workday system.

## Extend the Look up Workers action

Look up Workers action available along with the spoke provides most of the required inputs and outputs. Before adding more inputs and outputs to this action, explore ways to use the default spoke action.

This action transforms the input field data pills in the Workday HR spoke to the associated Workday request XML message and synchronously renders back the Workday response XML message as output field data pills in ServiceNow Workflow Studio. Ensure that you check the [Sample request message](https://community.workday.com/sites/default/files/file-hosting/productionapi/Human_Resources/v33.2/samples/Get_Workers_Request.xml) and [Sample response message](https://community.workday.com/sites/default/files/file-hosting/productionapi/Human_Resources/v33.2/samples/Get_Workers_Response.xml).

Modify or extend the default Look up Workers action by creating a copy of it.

![Create copy of the action.](../image/wd-hr-ex1.png)

To add Position Reference ID as part of the request criteria for this action:

**Note:**

-   Ensure that you check if the regular input field or the **Additional Field** input field has the desired input. If none of them have the desired input, perform these instructions to manually create the required input field.
-   The Look up Workers action supports Position Reference ID request element in the **Additional Fields** input field. For the purpose of demonstration, this field is manually being added in the UI.

1.  Evaluate and understand how Position Reference ID is structured in the [Workday request message](https://community.workday.com/sites/default/files/file-hosting/productionapi/Human_Resources/v33.2/samples/Get_Workers_Request.xml). The XPath to add a Position Reference ID in the request message is two-folded as per the [Workday Public Web Services community post](https://community.workday.com/sites/default/files/file-hosting/productionapi/Human_Resources/v33.2/Get_Workers.html#Get_Workers_RequestType).
    1.  [Position Reference Type attribute](https://community.workday.com/sites/default/files/file-hosting/productionapi/Human_Resources/v33.2/Get_Workers.html#Position_ElementObjectType): Get\_Workers\_Request/Request\_Criteria/Position\_Reference/@type
    2.  The attribute value above, per the Public Web Services doc, is a hard-coded “Position ID.”

        ![Position ID.](../image/wd-hr-ex1-posid.png)

    3.  Position Reference Value: Get\_Workers\_Request/Request\_Criteria/Position\_Reference
    4.  The actual value above is a new input field in the spoke action.
2.  Create an input variable in the **Action Input** step. Click **Create Input** and add a simple string type input variable.

    ![Create the Position Reference ID input.](../image/wd-hr-ex1-fd.png)

3.  Create an input variable in the Pre Processing script step.
    1.  Click **Create Variable**.
    2.  Add the input variable name with name as **position\_reference\_id**.
    3.  Drag the **Position Reference ID** data pill from **Input Variables** and drop it at the value of the input variable.

        ![Position Reference ID](../image/wd-hr-ex1-var.png)

4.  Leverage the design pattern of var organizationReferenceStr in the script section.
    1.  Create the XML node to match the [Workday Get Worker Request message](https://community.workday.com/sites/default/files/file-hosting/productionapi/Human_Resources/v33.2/samples/Get_Workers_Request.xml) in this example.
    2.  Find the appropriate design pattern in the script section accordingly. In this example, this XML node needs to be constructed for Position Reference.

        ```
        <bsvc:Position_Reference bsvc:Descriptor="string">
        <bsvc:ID bsvc:type="Position_ID">string</bsvc:ID>
        </bsvc:Position_Reference>
        
        ```

    3.  When the above XML is compared with the similar XML node, Organization Reference is a good candidate to leverage the associated design pattern script from. In the **Script** section, the associated script snippet is under “var organizationReferenceStr.

        ```
        <bsvc:Organization_Reference bsvc:Descriptor="string">
        <bsvc:ID bsvc:type="Organization_ID">string</bsvc:ID>
        </bsvc:Organization_Reference>
        
        ```

    4.  Leverage the var organizationReferenceStr code snippet to construct the Position Reference XML node accordingly.

        ![var organizationReferenceStr code snippet.](../image/wd-hr-ex1-var2.png)

    5.  On the same script, in the **var request** section, leverage the design pattern, and define an output variable.

        ![var request section.](../image/wd-hr-ex1-var3.png)

5.  Create the Position XML node in the SOAP Step.
    1.  Refer to [Workday Get Worker Request message](https://community.workday.com/sites/default/files/file-hosting/productionapi/Human_Resources/v33.2/samples/Get_Workers_Request.xml) and the position reference node accordingly.

        ![Position reference node.](../image/wd-hr-ex1-var4.png)

    2.  Save and publish it.
6.  Test the action.
    1.  As this is a data stream action, it should be tested using a flow. Create a sample flow with the action in it.

        ![Test action in a flow.](../image/wd-hr-ex1-test.png)

    2.  Provide **Position ID** and test the flow.

        ![Provide Position ID.](../image/wd-hr-ex1-test2.png)

    3.  Open the execution and navigate to SOAP step to check if the updated XML element node with position reference is created.

        ![Check execution.](../image/wd-hr-ex1-exec.png)


## Add and modify output fields of Workday spoke action

Extend the Workday spoke to retrieve the local first name and local last name.

1.  Evaluate and understand how the local name is structured in the [Workday response message](https://community.workday.com/sites/default/files/file-hosting/productionapi/Human_Resources/v33.2/samples/Get_Workers_Response.xml).
    -   Local First Name: The XPath for this element is Get\_Workers\_Response/Response\_Data/Worker/Worker\_Data/Personal\_Data/Name\_Data/Legal\_Name\_Data/Name\_Detail\_Data/Local\_Name\_Detail\_Data/First\_Name
    -   Local Last Name: The XPath for this element is Get\_Workers\_Response/Response\_Data/Worker/Worker\_Data/Personal\_Data/Name\_Data/Legal\_Name\_Data/Name\_Detail\_Data/Local\_Name\_Detail\_Data/Last\_Name
2.  Leverage the Legal Name design pattern in the Script Parser step and create the snippet for local legal name.

    ```
    var LocalFirstName = xmlDoc.getNodeText(Worker_DataXpath.concat("wd:Personal_Data/wd:Name_Data/wd:Legal_Name_Data/wd:Name_Detail_Data/wd:Local_Name_Detail_Data/wd:First_Name"));
            var LocalLastName = xmlDoc.getNodeText(Worker_DataXpath.concat("wd:Personal_Data/wd:Name_Data/wd:Legal_Name_Data/wd:Name_Detail_Data/wd:Local_Name_Detail_Data/wd:Last_Name"));
    
            var LocalLegalName = {
                LocalFirstName: LocalFirstName,
                LocalLastName: LocalLastName,
            };
    
    ```

    ![Legal Name design pattern in the Script Parser step.](../image/wd-hr-ex2.png)

3.  Add the LocalLegalName to the PersonalData object.

    ![LocalLegalName to the PersonalData object.](../image/wd-hr-ex2-2.png)

4.  Create output variables in the **Outputs** step.
    1.  Click **Edit Output**.
    2.  Output fields don't need to follow the exact Workday response message hierarchy. As long as the XPAth from the step 2 follows the right Workday XPath, the spoke action can render the elements accordingly. In this case, adding the **Local Legal Name** under **Personal Data** is sufficient.

        ![Output fields.](../image/wd-hr-ex2-3.png)

        **Note:** String variable name under the **Name** section must match with the same var name defined in step 2 above.

5.  Save and publish the action.

    **Note:** The Look up Workers action has a maximum number of output elements that a data stream action can have. If any error occurs during the publish of copied action with new output elements, delete a few output elements that are not required and try to publish again.

6.  Test the action.
    1.  Ensure that the testing worker subject has the local first name and local last name in Workday.
    2.  Create a sample flow, add the action to it, and log the response to verify output elements.

        ![Test the action.](../image/wd-hr-ex2-4.png)

    3.  Provide the associated test worker subject’s Employee ID to test and run the flow.

        ![Run the flow.](../image/wd-hr-ex2-5.png)

    4.  Verify the log and executions to verify if the local first name and local last name are retrieved correctly.

        ![Verify executions.](../image/wd-hr-ex2-6.png)


