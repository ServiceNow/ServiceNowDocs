---
title: PDF connector methods
description: Accelerate PDF processing for your document automation by using the various methods of PDF connector in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [PDF connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# PDF connector methods

Accelerate PDF processing for your document automation by using the various methods of PDF connector in RPA Desktop Design Studio.

## Prerequisites for using the PDF connector

Use the Load method in PDF connector before using the other methods. Call this method with the full path to the PDF file \(FilePath\) and optionally provide a password \(Password\) if the PDF is protected.

## Close

Closes the resources associated with the PDF document. Use this method to release any references and resources after using the Load method.

Call this method when you no longer need to use the PDF document or after completing operations with it.

## ConvertToExcel

Converts a PDF document to a Microsoft Excel document. Optionally, only tables can be converted if specified.

Call this method with the file path where the converted Excel document must be saved, and optionally set **ConvertTablesOnly** to **True** if only tables must be converted.

|Parameter|Description|Data type|
|---------|-----------|---------|
|ExcelFilepath|The file path where the converted Excel document \(.xlsx\) is saved. Ensure the file path includes the file name and extension.|String|
|ConvertTablesOnly|If set to **True**, only tables from the PDF document are converted to Excel. Default is **True**.|Boolean|

## ConvertToHTML

Converts a specified page of a PDF to HTML format. If the page number is less than or equal to 0, all pages of the PDF are converted to HTML.

Call this method with the page number of the PDF that you want to convert to HTML. If you pass a page number less than or equal to 0, the entire PDF will be converted to HTML. The method returns the HTML content as a string.

|Parameter|Description|Data type|
|---------|-----------|---------|
|PageNumber \(Data In\)|The page number of the PDF to be converted to HTML. If this parameter is less than or equal to 0, all pages of the PDF are converted to HTML. Page numbers typically start from 1.|Int32|
|Return \(Data Out\)|This method returns the HTML content as a string, representing the content of the PDF file.|String|

## ConvertToImage

Converts a specified page of a PDF document to an image. Optionally, specify the image path where the image is saved, DPI \(dots per inch\), and image quality.

Call this method with the page number of the PDF to convert, the file path where the image must be saved, and optionally adjust the DPI and image quality parameters.

|Parameter|Description|Data type|
|---------|-----------|---------|
|PageNumber|The page number of the PDF to be converted to an image. Page numbers typically start from 1.|Int32|
|ImagePath|The file path where the converted image is saved. Ensure the file path includes the file name and extension|String|
|Dpi|The DPI \(dots per inch\) resolution for the generated image. Default is 200 DPI.|Int32|
|Quality|The quality level of the generated image, ranging from 0 \(lowest\) to 100 \(highest\). Default is 95.|Int32|

## ConvertToImages

Converts a PDF document to images. Optionally, specify the folder path where the images are saved, DPI \(dots per inch\), image quality, and an optional list to store the generated file names.

Call this method with the folder path where the images must be saved. Optionally, adjust the DPI and image quality parameters. If you provide a list as the **FileNames** parameter, it is populated with the names of the generated image files.

<table id="table_jnw_jn5_krb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Folderpath

</td><td>

The folder path where the converted images will be saved. Ensure the folder exists and has appropriate write permissions.For example, `/Users/Username/Documents/MyFolder`

</td><td>

String

</td></tr><tr><td>

Dpi

</td><td>

The DPI \(dots per inch\) resolution for the generated images. Default is 200 DPI.

</td><td>

Int32

</td></tr><tr><td>

Quality

</td><td>

The quality level of the generated images, ranging from 0 \(lowest\) to 100 \(highest\). Default is 95.

</td><td>

Int32

</td></tr></tbody>
</table>## ConvertToWord

Converts a PDF to a Microsoft Word document.

Call this method with the file path where the converted Word document must be saved. The method creates a Word document from the PDF content at the specified path.

|Parameter|Description|Data type|
|---------|-----------|---------|
|WordFilepath|The file path where the converted Word document \(.doc\) is saved. Ensure the file path includes the file name and extension.|String|

## ConvertToXml

Converts a specified page of a PDF document to Microsoft XML format. Optionally, only tables can be converted if specified.

Call this method with the page number of the PDF to convert, the file path where the XML output must be saved, and optionally set **ConvertTablesOnly** to **True** if only tables must be converted.

|Parameter|Description|Data type|
|---------|-----------|---------|
|PageNumber|The page number of the PDF to be converted to XML format. Page numbers typically start from 1.|Int32|
|XmlFilePath|The file path where the converted XML document will be saved. Ensure the file path includes the file name and extension|String|
|ConvertTablesOnly|If set to True, only tables from the specified page will be converted to XML. Default is True.|Boolean|

## ExtractImages

Extracts images from specified pages of a PDF document. Optionally, specify the folder path where the images are saved and an output list to store the generated file names.

Call this method with the folder path where the images must be saved, the starting and ending page numbers from which to extract images, and an empty list to store the file names of the extracted images.

|Parameter|Description|Data type|
|---------|-----------|---------|
|Folderpath|The folder path where the extracted images are saved. Ensure the folder exists and has appropriate write permissions.|String|
|FromPage|The starting page number from which to extract images. Page numbers typically start from 1.|Int32|
|ToPage|The ending page number up to which images must be extracted. This number must be greater than or equal to the **FromPage** number.|Int32|
|FileNames|An output parameter that stores the file names of the extracted images.|List\`1|

## GetAllTables

Extracts all tables from a PDF document and returns them as a list of DataTables.

Use the **Return** parameter to retrieve the extracted table data as a list.

Call this method without any parameters to retrieve all tables from the PDF document. The method returns a list of DataTables, where each DataTable represents a table extracted from the PDF.

|Parameter|Description|Data type|
|---------|-----------|---------|
|Return|This method returns list of DataTable that represents a tables extracted from the PDF file.|List\`1|

## GetPageAsImage

Extracts data from a PDF document page and store it as an in-memory image.

Returns a specified page of a PDF document as an in-memory image.

Call this method with the page number of the PDF to retrieve the page as an image. The method returns the page as a System.Drawing.Image object.

|Parameter|Description|Data type|
|---------|-----------|---------|
|PageNumber|The page number of the PDF to be converted to an image. Page numbers typically start from 1.|Int32|
|Return|This method returns an image that represents a specified page of the PDF file.|Drawing.Image|

## GetPageCount

Retrieves the total number of pages in a PDF document. You must use the **Return** parameter to retrieve the total page count in the PDF as an integer.

|Parameter|Description|Data type|
|---------|-----------|---------|
|Return|This method returns an integer representing count of pages of the PDF file.|Int32|

## GetTable

Extracts a table from a PDF and returns it as a DataTable. The extraction method is specified by the **ExtractBy** parameter.

Call this method with the extraction type and the corresponding value. The method returns the extracted table as a DataTable.

<table id="table_z3v_4yg_3xb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

ExtractBy

</td><td>

The method of extraction to use. This parameter must be ExtractType, which includes the following options: Index \(0\) - extract by page number, and ContainsText \(1\) - extract by matching text.

</td><td>

ExtractType

</td></tr><tr><td>

Value

</td><td>

The value corresponding to the extraction type. For example, if **ExtractBy** is Index, this would be the page number as a string; if **ExtractBy** is ContainsText, this would be the text to match.

</td><td>

String

</td></tr><tr><td>

Return

</td><td>

This method returns a DataTable that represents a table extracted from the PDF file.

</td><td>

Table

</td></tr></tbody>
</table>## GetText

Retrieves text from the given range of PDF pages.

Call this method with the starting and ending page numbers to retrieve text from those pages. The method returns the extracted text as a string.

<table id="table_izn_yyg_3xb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

FromPage

</td><td>

The starting page number of the range from which to extract text. Page numbers typically start from 1.

</td><td>

Int32

</td></tr><tr><td>

ToPage

</td><td>

The page number to which you retrieve text from the start page. **Note:** Ensure that the ToPage value is higher than the **FromPage** value.

</td><td>

Int32

</td></tr><tr><td>

Return

</td><td>

This method returns a string representing the text content of the PDF file.

</td><td>

String

</td></tr></tbody>
</table>## Load

Loads a PDF file for interaction, enabling further operations such as extracting content.

Call this method with the full path to the PDF file \(FilePath\) and optionally provide a password \(Password\) if the PDF is protected.

|Parameter|Description|Data type|
|---------|-----------|---------|
|FilePath|The full path to the PDF file to be loaded. This must include the file name and extension.|String|
|Password|The password for the PDF file if it is protected. If the PDF is not password-protected, this parameter can be an empty string.|String|

## Merge

Merges a list of PDF files into a single PDF file.

Call this method with a list of file paths of the PDFs to be merged, the output file path, and an optional overwrite flag.

<table id="table_bny_zmh_3xb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

FileList

</td><td>

A list of file paths for the PDF files to be merged. Each path must be a valid path to a PDF file.

</td><td>

ArrayList

</td></tr><tr><td>

OutputFilePath

</td><td>

The file path where the merged PDF is saved. This must include the file name and extension.

</td><td>

String

</td></tr><tr><td>

Overwrite

</td><td>

If set to **True**, the method overwrites the existing file at the output path if it exists. If set to **False**, the method does not overwrite the existing file. Default is **False**.

</td><td>

Boolean

</td></tr></tbody>
</table>**Note:** If the PDF files are password protected or in an incorrect format in the **FileList** parameter, the automation displays an error.

## Split

Splits a single PDF into multiple files, where each page in the PDF is saved as a separate file.

Call this method with the output folder path where the split PDF pages must be saved.

|Parameter|Description|Data type|
|---------|-----------|---------|
|OutputFolderPath|The path to the folder where the split PDF pages are saved. Ensure the folder exists or has appropriate permissions for writing files.|String|

**Parent Topic:**[PDF connector](pdf-connector.md)

