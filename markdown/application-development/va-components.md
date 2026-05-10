---
title: Develop a component for Virtual Agent
description: Create a custom Virtual Agent component to gather input or display information in the Virtual Agent client interface.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Create custom components using ServiceNow CLI, Builder library, Developing your application, Building applications]
---

# Develop a component for Virtual Agent

Create a custom Virtual Agent component to gather input or display information in the Virtual Agent client interface.

## Types of Virtual Agent components

To develop a component for Virtual Agent, add specific properties and actions to interact with the Virtual Agent client interface. The properties required depend on the type of component you are creating.

-   **Response component**

    A response component only provides information to the user, and does not gather input or handle user interaction. For example, a card control that does not require user input and is only in the conversation once.![A card control as an output component that does not require user input](../image/card-control.png)

    Add a property to your response component to handle the data sent by the Virtual Agent server.

<table id="table_dql_lqd_lmb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

controlData

</td><td>

Initial data that the Virtual Agent server sends to your component as the topic runs. Data type: JSON Object

</td></tr></tbody>
</table>-   **Input component**

    An input component displays information and/or gathers user input. It includes the same property as the output component to handle data sent by the server, but has more possible states and requires user interaction.

<table id="table_k3t_nqd_lmb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

controlData

</td><td>

Initial data that the Virtual Agent server sends to your component as the topic runs. Data type: JSON Object

</td></tr><tr><td>

responseValue

</td><td>

Data sent to the component from the user's response, either from the client directly, or from the server if there is a refresh. Only use in components that require user input. Data type: JSON Object

</td></tr><tr><td>

forceCloseControl

</td><td>

Flag that indicates whether the component can accept input. When true, the control closes and the user cannot interact with it. Monitor changes on the client to update this value. Only use in components that require user input.Data type: Boolean

</td></tr></tbody>
</table>    Use this action to emit data from user interaction.

<table id="table_pdz_frd_lmb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

VA\_CONTROL\#VALUE\_SENT

</td><td>

Response data from the client to send to the server. Only use in components that require user input. Data type: JSON Object

</td></tr></tbody>
</table>
## Input component states

Because they accept data, input components must handle multiple states. The state flow is generally as follows:

1.  Virtual Agent shows the custom component in the waiting for input state.
2.  The user interacts with the component to provide input.
3.  The component closes and sends the `responseValue` property to the server.
4.  The server runs the server-side logic and sends the component with the user's input back to the client.

-   **Waiting for Input**

    The initial state of a component waiting for user interaction. The `controlData` property is set, but the `forceControlClosed` property is false. This example shows a slider component in the waiting for input state.

    ![Component waiting for input.](../image/slider-open.png)

    In this example, if the user has not provided a `responseValue` and the control is not closed, the slider and the input button display.

    ```
    const {controlClosed, sliderVal, sliderMin, sliderMax} = state;
    return (<div class={{"slider-chat": true}}>
        {responseValue ? null :  <Fragment>
        <div class={{"slider-label": true}}>{label}</div>
        {controlClosed ? null : <Fragment>
            <div class={{"slider-container": true}}>
                        <input on-change={onSliderChange} type="range" min={sliderMin} max={sliderMax} value={sliderVal} class={{"slider": true}} />
                <div class={{"slider-value": true}}>
                        {unitIcon && 
                         <div class={{"unit-icon": true}}><img src={unitIcon} /></div>
                         } 
                         {sliderVal} {unitName}
                    </div>
            <div class={{"button-container":true}}>
                <now-button variant="primary" label={buttonText || 'Confirm'} />
             </div></div></Fragment>}
    ```

-   **Handling Input**

    In the previous example, the slider uses a `now-button` component, which the user clicks to confirm input and send it to the server. When the user clicks the button, the `VA_CONTROL#VALUE_SENT` action fires with the `responseValue` payload.

    ```
    'NOW_BUTTON#CLICKED': (data) => {
        const {updateState, dispatch, state: {sliderVal}} = data;
        updateState({controlClosed: true});
        dispatch('VA_CONTROL#VALUE_SENT', {
            value: {
                sliderVal
            }
        }); 
    }
    ```

-   **Closed**

    A component that is closed can no longer accept user input. Components are generally closed because:

    -   The user responded to the component. The component closes and the conversation continues.
    -   The user ended the chat. The server does not wait for a response.
    For example, the slider component only renders the original prompt when in the closed state.

    ![Closed component that is no longer waiting on user input.](../image/closed-slider.png)

-   **Sending response**

    After the user responds, the control is rendered again on the user's side of the conversation with the value of the `responseValue` property.

    ![Users response sent to the client.](../image/input-control-response.png)

    For example, the slider control uses this snippet to render the response.

    ```
    {responseValue && <div className="response-container slider-value">
       {unitIcon && 
       <div className="unit-icon"><img src={unitIcon} /></div>
       } 
       {returnVal} {unitName}
    </div>}
    ```


## Adding the component to Virtual Agent Designer

After developing the component and deploying it to your instance, add it to Virtual Agent Designer using a custom control and definition. For more information, see [Virtual Agent custom controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/custom-controls.md).

-   **[Add properties to communicate with Virtual Agent](../task/add-va-properties.md)**  
To develop a component for Virtual Agent, add specific properties and actions to interact with the Virtual Agent client interface. The properties required depend on the type of component you are creating.
-   **[Test a component for Virtual Agent](../task/test-va-component.md)**  
Test your Virtual Agent custom component before deploying it to your instance.

**Parent Topic:**[Create custom components using ServiceNow CLI](custom-components.md)

