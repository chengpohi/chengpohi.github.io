---
description: EDQL's Import Feature for Elasticsearch Index
---

# Import

<figure><img src="/.gitbook/assets/image-(5).png" alt=""><figcaption></figcaption></figure>

EDQL provides a robust import feature that simplifies the process of importing documents into an Elasticsearch index. Here's a step-by-step guide on how to use this feature:

1. Connect to Elasticsearch: Launch the EDQL Dock Manager and establish a connection with your Elasticsearch cluster. Double-click the connection node to configure and establish the connection.
2. Select the target index: Navigate to the desired index within the EDQL Dock Manager. Right-click on the index node to open the context menu.
3. Choose "Import" option: From the context menu, select the "Import" option. This action will open the import dialog specific to the selected index.
4. Specify the import file format: In the import dialog, choose the file format of your documents. EDQL currently supports CSV and Excel formats for importing.
5. Select the import file: Browse your system and select the CSV or Excel file containing the documents you want to import. Ensure that the file adheres to the expected format, with the first line containing field names and subsequent lines containing the corresponding document data.
6. Start the import: Click the "Import" or "Start" button within the import dialog to initiate the import process. EDQL will read the file and automatically map the fields in the first line to the index properties in Elasticsearch.
7. Monitor the import progress: The import dialog will display a progress bar indicating the import progress. You can monitor this progress to track the completion status.
8. Cancel the import (if needed): If you need to cancel the import process for any reason, you can click the "Cancel" or "Stop" button within the import dialog. This action will halt the import, allowing you to abort the operation.
9. Verify the import: Once the import is complete, you can verify the imported documents by querying the Elasticsearch index using EDQL or any other Elasticsearch querying tool.

EDQL's import feature streamlines the process of importing documents into your Elasticsearch index. It provides support for CSV and Excel formats, allowing you to easily import structured data.&#x20;
