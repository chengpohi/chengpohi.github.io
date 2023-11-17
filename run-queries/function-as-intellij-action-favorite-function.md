---
description: quickly run function with params by action shortcut
---

# Function as Intellij Action: Favorite Function

EDQL has introduced a powerful feature that integrates EDQL functions seamlessly into the IntelliJ IDE, providing a familiar and efficient environment for query development. With EDQL Function as IntelliJ Action, developers can write, execute, and manage their EDQL functions directly within IntelliJ, leveraging the IDE's rich features and enhancing productivity. This integration enables a streamlined workflow, eliminating the need to switch between multiple tools and enhancing the overall developer experience. EDQL Function as IntelliJ Action empowers you to develop Elasticsearch queries with ease and efficiency.

<figure><img src="/.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

<figure><img src="/.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

## 1. Launch EDQL and Open the Editor

\
Open EDQL and navigate to the editor section where you can create and edit your functions.

## 2. Create a Function

\
In the editor, create a new function by typing the following code:

```
function getIds() {
  POST fff/_search
  {}
}
```

This function sends a POST request to the "fff/\_search" endpoint with an empty request body. Modify the endpoint and request body as per your specific requirements.

## 3. Save the Function

\
Click on the "Save" button or use the appropriate keyboard shortcut to save your function. Give it a meaningful name, such as "getIds".

## 4. Assign the Function as a Favorite

\
In the editor's right sidebar, locate the favorite icon associated with the "getIds" function. Click on the favorite icon to mark the function as a favorite.

## 5. Execute the Function

\
To execute the function, you have a couple of options:

* Option 1: Using Keyboard Shortcut
  * Press "Cmd+A" (Mac) or "Ctrl+A" (Windows) to select the entire function code.
  * Press "Enter" or click the "Run" button to execute the selected function.
* Option 2: Using Favorite Icon
  * Click on the favorite icon in the right sidebar to select the entire function code.
  * Press "Enter" or click the "Run" button to execute the selected function.

## 6. Input Parameters (if applicable)

\
If your function requires input parameters, a parameter dialog may appear after executing the function. Enter the specific parameter values as required or use the existing parameters if applicable.

## 7. Run or Cancel the Execution

\
In the parameter dialog, click the "Run" button to execute the function with the provided parameters. If you wish to cancel the execution, click the "Cancel" button.

That's it! You have created a function in EDQL, marked it as a favorite, and executed it using the keyboard shortcut or favorite icon. You can input parameters for the function and choose to run or cancel the execution as needed.
