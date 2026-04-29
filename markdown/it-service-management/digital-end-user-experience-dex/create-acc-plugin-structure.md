---
title: Create an ACC plugin package
description: Create an Agent Client Collector \(ACC\) plugin package that includes the PowerShell script defining the remedial action, a Ruby script, and an allowlist to enable execution of the remedial action on an endpoint device.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Creating and executing a PowerShell script-based remedial action, DEX remedial actions, Configure, Digital End-User Experience, IT Service Management]
---

# Create an ACC plugin package

Create an Agent Client Collector \(ACC\) plugin package that includes the PowerShell script defining the remedial action, a Ruby script, and an allowlist to enable execution of the remedial action on an endpoint device.

## Before you begin

Role required: admin

## Procedure

1.  Create a root folder for the ACC plugin in your local computer and name it.

    For example, `acc-dex-custom`.

2.  In the root folder, create two sub-folders named `allowlist` and `bin`.

3.  Create a PowerShell script using PowerShell or command prompt commands to define the remedial action to run on an endpoint device.

    1.  In the `bin` folder, create a `.ps1` file and name it with the `.ps1` extension.

        For example, `CustomScript.ps1`

    2.  Open the `.ps1` file and add the commands.

        For example, the following sample `.ps1` file defines a custom remedial action using commands to stop and start the W32Time process, pause, and restart the Spooler service on a device.

        ```
        sc.exe stop w32time
        
        $process = Get-Process -Name w32time -ErrorAction SilentlyContinue
        if ($process) {
            taskkill /f /t /im w32tm.exe
        }
        
        Start-Sleep -Seconds 5
        
        sc.exe start w32time
        Start-Process "C:\Windows\System32\w32tm.exe"
        
        Start-Sleep -Seconds 5
        
        sc.exe stop spooler
        sc.exe start spooler
        ```

        **Note:** You can configure the PowerShell script to accept input parameters defined in the ServiceNow instance during execution.

    3.  Save the file.

4.  Create a Ruby script to call the `.ps1` file from the ServiceNow instance.

    1.  In the `bin` folder, create a Ruby file and name it with the `.rb` extension.

    2.  Open the `.rb` file and add your code using plain Ruby or any Ruby framework.

        The Ruby script must include the logic to:

        -   Call the `.ps1` script you created, making sure that you enter the correct file path.
        -   Validate if the command is successfully executed.
        -   Create an output JSON that includes the execution status, output, and errors, if any.
    3.  Execute the command and review the output to confirm if the `.ps1` file is called successfully or if there are any errors.

        For example, the following sample `.rb` file runs a `.ps1` file \(`CustomScript.ps1`\) using the acc-f-commons plugin run command, validates if the command runs successfully, and returns the result JSON.

        ```
        require "logger"
        require_relative "../../../acc-f-commons/bin/command_runner.rb"
        require "json"
        
        class CustomScript
          def initialize()
            @logger = Logger.new(STDOUT)
            @cmd_runner = CommandRunner.new
            @logger.level = "FATAL"
          end
        
          def execute_custom_script()
            status = "failure"
            msg = nil
            data = {}
        
            parent_cache_directory = File.expand_path("../..", File.dirname(__FILE__)).gsub(" ", "` ")
            query = "powershell -ExecutionPolicy Bypass " + parent_cache_directory + "/acc-dex-custom/bin/ps/customScript.ps1"
        
            output, error = @cmd_runner.runCmd(query, @logger, "mode con:cols=32766 lines=1 & chcp 65001 > nul & ", true, false)
        
            if !error && !output.empty?
              status = "success"
              msg = "Successfully ran script"
              data = output
            else
              msg = "Failed - #{error}"
            end
        
            result = {
              "status" => status,
              "type" => "device",
              "metric_type" => "remedial_action",
              "keys" => "custom_script",
              "data" => data,
              "message" => msg
            }
        
            puts JSON.generate(result)
          end
        end
        
        custom_script = CustomScript.new
        custom_script.execute_custom_script()
        ```

        **Note:**

        If the PowerShell script is configured to accept input parameters from the ServiceNow instance, the Ruby script passes these parameters to the PowerShell script during execution.

5.  Create an allowlist file and specify the Ruby script permitted for execution on endpoint devices.

    1.  In the `allowlist` sub-folder, create an allowlist JSON file.

        For example, `check-allowlist.json`.

    2.  Define any conditions such as arguments to be accepted as part of the `.rb` script, or create a custom logic.

    3.  Save the file.

6.  Generate a `tar.gz` file for your ACC plugin folder using any utility.

    **Note:** The `tar.gz` file name must match the plugin root folder name. For example, `acc-dex-custom.tar.gz`


**Parent Topic:**[Creating and executing a PowerShell script-based remedial action](../concept/remedial-actions-ps.md)

