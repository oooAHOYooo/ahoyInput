## ahoyInput
the internal tool to update ahoy

#Tool 1 = Audio Json Editor

Given the structure of your JSON file, the JavaScript code will extract the provided JSON file, allow the user to add a new song entry via a form, and then export the updated data as a new JSON file. The HTML and JavaScript code below is tailored to match the structure of your JSON file:

#In this setup:

The user first uploads the existing JSON file.
The handleFile function reads the file and populates the library object with the existing data.
The song submission form and the "Export to JSON" button are then revealed.
When the form is submitted, the new song data is added to the library object.
Clicking the "Export to JSON" button triggers the exportToJson function, which creates a download link for the updated JSON file.
This setup allows for client-side reading, writing, and exporting of a JSON file, all within the constraints of browser security restrictions

# About

However, it's essential to note that this solution has some limitations:

Manual Process: Each time you want to update the JSON file, you'll need to manually upload the existing file, add the new entries, and then manually download and replace the old file with the updated one wherever it's hosted or used in your app.
No Server-side Validation: As a client-side solution, it lacks server-side validation, which can be a crucial factor if you want to ensure data integrity and security.
No Persistent Storage: There's no persistent storage or database involved; the data only exists in the JSON file. If the user navigates away from the page or closes their browser, any unsaved changes will be lost.
No Multi-user Support: Multiple users cannot update the library simultaneously as there's no backend to handle concurrent updates.
