# Create and auto-REST enable a table
<!-- WMSID 4602 -->
## Introduction

In this lab, you will use Database Actions/SQL Developer Web to:

- Connect to your database
- Create a table
- REST-enable the table

Estimated Lab Time: 20 minutes

Watch the video below for a quick walk-through of the lab.
[Create and auto-REST enable a table](videohub:1_7agj8yum)

### Objectives

- Create a table
- Auto-REST enable a table

### Prerequisites

- The following lab requires an [Oracle Cloud account](https://www.oracle.com/cloud/free/). You may use your own cloud account, a cloud account obtained through a trial, or a training account whose details were given to you by an Oracle instructor.

- This lab assumes you have completed all previous Labs.

## Task 1: Create a Table in the Autonomous Database

1. Sign in to [Database Actions](https://oracle-livelabs.github.io/common/labs/sqldevweb-login/sqldevweb-login.md) as the **ADMIN** user and navigate to the SQL Worksheet. You can also do this from within the OCI Cloud Console.

    ![access-sql-worksheet-from-oci-console](images/access-sql-worksheet-from-oci-console.png " ")

    > **NOTE:** If this is your first time accessing the SQL Worksheet, you will be
    > presented with a guided tour. Complete the tour or click the X in any
    > tour popup window to quit the tour.

     ![first-time-logging-in-to-sql-worksheet-as-admin-user](images/first-time-logging-in-to-sql-worksheet-as-admin-user.png " ")

2. Save the following [CSV file](https://c4u04.objectstorage.us-ashburn-1.oci.customer-oci.com/p/EcTjWk2IuZPZeNnD_fYMcgUhdNDIDA6rt9gaFj_WZMiL7VvxPBNMY60837hu5hga/n/c4u04/b/livelabsfiles/o/developer-library/csv_data.csv), locally.

3. Next, click the **Data Load** button in the SQL Worksheet to load the CSV data into a new table.

    ![Click Data Loading Tab on SQL Worksheet](images/click-data-load-button-to-load-new-table.png " ")

4. A Data loading slider will appear. Drag and drop the CSV file into the Data loading slider window.

    ![drag-and-drop-csv-file-into-data-load-slider](images/drag-and-drop-csv-file-into-data-load-slider.png " " )

5. The `csv_data.csv` file will appear as "pending." Next, select `Settings` from the kebab menu icon.

    ![click-settings-option-from-kebab-menu-in-data-load-slider](./images/click-settings-option-from-kebab-menu-in-data-load-slider.png " ")

6. Review the File Preview page, then click `Next`.

    ![review-the-csv-data-before-reviewing-datatype-info](./images/review-the-csv-data-before-reviewing-datatype-info.png " ")

7. Review the Table name; it should be named `CSV_DATA`. Next, review the column names and data types. Once you've verified that everything is correct, click the `Save Settings` button.

    ![reviewing-datatype-info-for-new-csv-table](./images/reviewing-datatype-info-for-new-csv-table.png " ")

8. Next, click the `Upload` button. The `CSV_DATA` create table job will transition from "Pending" to "Uploaded. Once complete, click the `Close` button.

    ![click-the-upload-button-once-checked-for-accuracy](./images/click-the-upload-button-once-checked-for-accuracy.png " ")

    ![uploaded-success-screen-in-data-load-slider](./images/uploaded-success-screen-in-data-load-slider.png " ")

## Task 2: Review using the User Interface

1. We can view our newly created table and its data using the navigator on the left of the SQL Worksheet. Right-click the table name `CSV_DATA` and select `Open` from the popup menu.

    ![Using the navigator on the left of the SQL Worksheet, we can see out new table](./images/navigating-reviewing-new-table.png)

    The right side of the page will display a slider. You can review the data definition (DDL), triggers, constraints, and data.

    ![Click the Data option to view the table data](./images/table-options-slider.png)

## Task 3: Auto-REST Enable a Table

1. Next, you'll Auto-REST enable the `CSV_DATA` table. From the Navigator tab, locate the `CSV_DATA` table.

    ![Using the navigator on the left of the SQL Worksheet, find the CSV_DATA Table](./images/using-navigator-to-find-table.png)

2. Right click on the table name and select **REST** in the popup menu then **Enable**.

    ![Right click on the table name and select REST in the pop up menu then Enable](./images/rest-enabling-table.png)

3. A REST Enable Object slider will appear from the right side of the page. Keep the default values, then click the **Enable** button on the slider.

    ![The REST Enable Object Slider, view the Preview URL](./images/rest-enable-slider-context.png)

4. The `CSV_DATA` table is now Auto-REST enabled. You'll interact with the `CSV_DATA` table's REST endpoints in later labs with cURL commands. You can view the available REST endpoints by right-clicking the table name, selecting **REST**, then **cURL command**.

    ![Right click the table name in the navigator, select REST, then cURL Command](./images/retrieve-curl-command-for-object.png)

    > **NOTE:** Notice the available cURL commands and options for various shell
    > environments: Command Prompt, PowerShell, and Bash.

      ![The Command Prompt cURL for the table CSV_DATA side out panel](./images/command-prompt-curl-command.png)
      *Command Prompt*

      ![The PowerShell cURL for the table CSV_DATA side out panel](./images/powershell-curl-command.png)
      *PowerShell*

      ![The Bash cURL for the table CSV_DATA side out panel](./images/bash-curl-command.png)
      *Bash or Zsh*

5. You can also view this ORDS-enabled table from your browser. Copy the URL portion of the `GET` cURL command. Place this URL in a new browser window or tab.

   ![URL portion of cURL command in a new browser window.](images/curl-in-new-browser-tab-or-window.png)

6. You may also review the JSON representation using your browser's Developer Tools. This should give you a good idea of how the data is structured and how it will be presented to a user, a "client," or an application.

   ![Viewing results from a table in new browser with developer tools.](images/viewing-results-from-table-in-browser-and-dev-tools.png)

7. In The next lab, you will learn about using a **BATCH LOAD** endpoint.

You may now [proceed to the next lab](#next).

## Acknowledgements

### Author

- Jeff "el jefe" Smith, Distinguished Product Manager
- Chris Hoina, Senior Product Manager

### Last Updated By/Date

- Chris Hoina, August 2024
