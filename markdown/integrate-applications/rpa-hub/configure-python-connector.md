---
title: Configure the Python connector
description: Write and validate custom Python scripts and execute them as part of your automation by using the Python connector in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Python connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Configure the Python connector

Write and validate custom Python scripts and execute them as part of your automation by using the Python connector in RPA Desktop Design Studio.

## Before you begin

Ensure you have installed the Scripting plugin on the RPA Desktop Design Studio. To install, see [Manage plugins in RPA Desktop Design Studio](install-plugins-rpa-studio.md).

Ensure that a Python version is installed on your machine which is a part of the environment variables. For more information about environment variables, see [Setting environment variables](https://docs.python.org/3/using/windows.html#configuring-python).

Familiarize yourself with the limitations of Python script. For more information, see [Limitations of Python script in Python connector](../reference/python-script-limitations-rpa.md).

Role required: none

## Procedure

1.  In the Toolbox pane, navigate to **Connectors** &gt; **Python**

2.  Drag the Python component under the Global Objects in the Project Explorer pane.

3.  Right-click the Python connector.

4.  Click **Configure**.

    The Script Editor window is displayed.

    If Python is not installed on your machine, you will encounter an error message. Please install Python and reload the project again.

5.  In the **Python Version** list, select a version that is installed or available on the end user's machine, can run the automation, and is the same or higher than the runtime version.

    **Note:**

    You view a list of installed python versions on your machine in the Python Version list.

    Python versions 2.7 and above are supported. If your script is not validating or executing, ensure you are using version 2.7 or a higher version.

    By default, the highest installed Python version is selected.

    If you select version 2.x and have Python 3.x installed on your machine, the automation will run, but the Python script may not execute. The script will only execute if it is compatible with Python 3.x; otherwise, you may encounter an error.

    During the execution of the automation, if you select a specific version, such as 3.15.3, and have Python 3.11.3 installed on your machine, the automation will not run, and you will encounter an error. To proceed, select the same version, 3.15.3, or a higher version of Python.

    You can view the python version that is used for execution in the Studio logs, that is created in your user profile on your machine.

    ![Script pane and Python Version in Script Editor.](../image/python-script-editor-studio.png "Script pane and Python Version in Script Editor")

6.  Enter the custom script in the Script pane.

    Example script for temperature conversion and weather advice.

    ```
    
    def celsius_to_fahrenheit(temp_c: float) -> float:
        """
        Convert a temperature from Celsius to Fahrenheit.    
        Args:
            temp_c (float): Temperature in Celsius.
        Returns:
            float: Temperature in Fahrenheit.
        """
        return (temp_c * 9/5) + 32
    
    
    class WeatherAdvisor:
        """
        A simple class that provides weather advice based on temperature and conditions.
        """
    
        def give_advice(self, city: str, temperature_c: float, is_raining: bool, wind_speed: int) -> str:
            """
            Provide advice based on weather conditions.
            Args:
                city (str): The name of the city.
                temperature_c (float): Current temperature in Celsius.
                is_raining (bool): Whether it is raining.
                wind_speed (int): Wind speed in km/h.
            Returns:
                str: Weather advice message.
            """
            temp_f = celsius_to_fahrenheit(temperature_c)
    
            advice = f"In {city}, it is {temperature_c:.1f}°C ({temp_f:.1f}°F). "
    
            if is_raining:
                advice += "Take an umbrella. "
            else:
                advice += "No rain today. "
    
            if wind_speed > 30:
                advice += "It’s quite windy, be cautious!"
            else:
                advice += "Winds are calm."
    
            return advice
    
    
    # Example usage
    if __name__ == "__main__":
        advisor = WeatherAdvisor()
    
        message = advisor.give_advice(
            city="London",
            temperature_c=18.5,
            is_raining=True,
            wind_speed=25
        )
    
        print(message)
     
    ```

7.  Select **Validate**.

    If your custom script has any errors, it is displayed in the Errors pane. Resolve the errors and select **Validate** to check for errors again.

8.  Click **OK**.

    If you want to save the changes, select **Yes**. The code is validated. If you want to discard the changes, select **No**.

9.  Double-click the Python connector to expose the methods under the Object Explorer pane.

10. Drag the methods to the Design surface.

    For more information about Python connector methods, see [Python connector methods](../reference/python-connector-methods-rpa.md).


## Temperature conversion and weather advice

Perform the following steps to execute the automation for temperature conversion and weather advice.

1.  In the Toolbox pane, navigate to **General** &gt; **Variable**.
2.  Drag Variable component to the design surface.
3.  Double-click the Variable component and set these parameters as shown in the image.

    ![Parameters such as Temperature, City, isRaining, and WindSpeed are set in the Variable Container.](../image/variable-parameters-python-rpa.png "Parameters for Variable Container")

4.  Double-click the Python connector in the Global Objects.
5.  Drag the Execute method from Object Explorer to design surface.
6.  Select the component and click the method settings icon \(![Method settings icon](../image/component-settings-icon.png)\) or double-click the component head bar.
7.  Select the **Show Functions** check box and select the **celsius\_to\_fahrenheit** function from the Functions list.
8.  Select **OK**.
9.  Drag the Execute method again from Object Explorer to design surface.
10. Select the **Show Functions** check box and select the **celsius\_to\_fahrenheit** function from the Functions list.
11. Select **WeatherAdvisor** option from the Classes list.
12. Select **give\_advice** option from the Methods list.
13. Select **OK**.
14. Connect the ports of the components as shown in the following image.

    ![Python connector automation example.](../image/weather-example-python-rpa.png "Ports connection for Variable component and Execute methods")

15. To test the component, right-click the Variable component and select **Run From Here**.

    ![Temperature is displayed on the Data Out port of Execute method.](../image/weather-result-temp-python-rpa.png "Example result for temperature")

    ![Weather advice is displayed on the Data Out port of Execute method.](../image/weather-advice-python-rpa.png "Example result for weather advice")


**Parent Topic:**[Python connector](../concept/python-connector-rpa.md)

