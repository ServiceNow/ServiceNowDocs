---
title: Python connector methods
description: Execute custom Python scripts or files as part of an automation workflow by using the methods of Python connector in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-08-14"
reading_time_minutes: 3
breadcrumb: [Python connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Python connector methods

Execute custom Python scripts or files as part of an automation workflow by using the methods of Python connector in RPA Desktop Design Studio.

## Prerequisites for using the Python connector methods

Configure the Python connector. For more information, see [Configure the Python connector](../task/configure-python-connector.md).

Familiarize yourself with the limitations of Python script. For more information, see [Limitations of Python script in Python connector](python-script-limitations-rpa.md).

## Execute

Executes Python scripts set up in the configuration window. Before executing the method, you must configure the connector. See [Configure the Python connector](../task/configure-python-connector.md).

To execute, do the following steps.

1.  Select the component and click the method settings icon \(![Method settings icon](../image/component-settings-icon.png)\) or double-click the component head bar.
2.  From the **Classes** list, select the class defined during the configuration of the Python connector.

    For example, **Math**.

3.  From the **Methods** list, select the method defined during the configuration of the Python connector.

    For example, **add**.

4.  Select the **Show Functions** check box and select a function from the **Functions** list.

    Functions are those methods that are not written within a class. For example, banner.

    ![Banner function is selected from the Functions list.](../image/show-functions-python-rpa.png "Show Functions check box")

    ![Function in Execute Method.](../image/execute-python-script.png "Function in Execute Method")

5.  Click **Validate**.
6.  Click **OK**.

    A Data Out port \(Result\) is created to return the output.

7.  To test the method, right-click the Execute method and select **Run From Here**.

<table id="table_ksp_35h_ltb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Result

</td><td>

Returns the output of the script.!["Welcome Abel Tutor" is displayed in the Data Out port of the Execute method.](../image/execute-method-result-rpa.png "Result of the Execute method")

</td><td>

Data Out

</td><td>

String

</td></tr></tbody>
</table>## InvokeScript

Runs the Python script on local computers and gets the output. Ensure that the Python file is available in the file path provided.

Ensure that a Python version is installed on your machine. You must ensure that the Python script is running without errors.

![InvokeScript method.](../image/invokescript-python-connector.png "InvokeScript method")

<table id="table_a3f_lbn_jgc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Script

</td><td>

Returns the output of the script. The command specified in the Script parameter for execution via the InvokeScript component is same as the command line that is used to run in a command prompt.

Provide a file path for the Python script. For example, `python "C:\Users\abel.tutor\Downloads\utility_runner.py"`

For example, `py -3 "C:\Python testing\project1\main.py" Abel` it has &lt;python with version&gt; &lt;python file path&gt; &lt;arguments&gt; format. For adding multiple arguments, use space.

Example of a Python script that greets the user, returns current time, and performs calculations of add and multiply.

```
# utility_runner.py

import datetime

# Top-level function
def greet_user(name):
    print(f"Hello, {name}!")

# Another top-level function
def get_current_time():
    print(f"Current time: {datetime.datetime.now().strftime('%Y-%m-%d %H:%M:%S')}")

# Class with methods
class Calculator:
    def __init__(self, a, b):
        self.a = a
        self.b = b

    def add(self):
        print(f"Addition: {self.a + self.b}")

    def multiply(self):
        print(f"Multiplication: {self.a * self.b}")

# Run all functions and methods in sequence
def run_all():
    greet_user("Abel.Tutor")
    get_current_time()

    calc = Calculator(5, 3)
    calc.add()
    calc.multiply()

if __name__ == "__main__":
    run_all()

```

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

Return

</td><td>

Output of the script that is returned.![Result is displayed in the Data Out port of the InvokeScript method.](../image/invokescript-method-result-rpa.png "Result of the InvokeScript method")

</td><td>

Data Out

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Python connector](../concept/python-connector-rpa.md)

