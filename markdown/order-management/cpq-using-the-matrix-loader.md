---
title: Configure the Matrix Loader
description: Use the Matrix Loader to efficiently add, edit, and migrate fields, field options, rules, and layouts in CPQ. Upload CSV files, validate configurations, and streamline bulk updates or environment migrations with error-handling and verification support.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configure the Matrix Loader

Use the Matrix Loader to efficiently add, edit, and migrate fields, field options, rules, and layouts in CPQ. Upload CSV files, validate configurations, and streamline bulk updates or environment migrations with error-handling and verification support.

The Matrix Loader is the most efficient means of adding and editing fields, field options, rules, and layouts, particularly when the number of elements gets large. When using the Matrix Loader, administrators define their configuration elements in a spreadsheet file. This spreadsheet artifact provides a backup of data in CPQ; it also facilitates fast test-to-production migration processes.

Here is a quick tutorial on how to use the Matrix Loader.

1.  Click **Matrix Loader** in the navigation pane.

    ![Menu](../images/cpq-matrix-loader.png)

2.  On the page that opens, export sample files in the upload formats that are accepted by the Matrix Loader: fields, field options, rules, and tables. Each sample file demonstrates a broad range of the features of the upload format.

    ![Sample files](../images/cpq-matrix-loader-tutorial-sample-files.png)

3.  Drag, or use the file browser to select the CSV files you intend to upload.

    ![Drag and drop or use the file browser to select the CSV files](../images/cpq-matrix-loader-tutorial-choose-files.png)

    We discuss the formats of these CSV files in the following articles:

    -   [Matrix Loader CSV fields and field options upload and export](cpq-matrix-loader-csv-fields-and-field-options-upload-and-export.md)
    -   [Matrix Loader: CSV rules upload](matrix_loader_csv_rules_upload.md)
    -   [Matrix Loader: CSV table upload](../task/cpq-matrix-loader-csv-table-upload.md)
    Queued files are displayed. If necessary, add more files or delete files, and then click **Next**.![Import](../images/cpq-matrix-loader-tutorial-choose-files-selected-files-shown.png)

4.  The Matrix Loader guesses at the contents of each file according to keywords in the file titles. Confirm that the Matrix Loader guessed the upload file types correctly. If necessary, make corrections.

    The Matrix Loader performs the uploads in the sequence necessary to ensure all elements are uploaded correctly. Click **Import**.

    ![Import user interface](../images/cpq-matrix-loader-tutorial-confirm-type.png)

5.  Confirm that all the uploads succeeded. Most errors originate in a mistake or mismatch in an upload file. When all uploads have succeeded, click **Continue**.![Import files](../images/cpq-matrix-loader-tutorial-import-files.png)
6.  In the appropriate administration areas \(fields and rules, if you uploaded these ﬁles\), check and confirm the elements that were created as a result of this Matrix Loader upload.

**Related topics**  


[Matrix Loader](matrix_loader_table_of_contents.md)

