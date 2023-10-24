# Apimio_Task

This readme file provides an overview of the web project, Apimio_Task, which is currently live on Vercel. The project includes a user interface with various elements, such as buttons, a video player, and links. It also features functionality for tracking user interactions and displaying the interactions in a dashboard. You can access the live project on Vercel using this Url:https://apimio-task.vercel.app/

# several approaches and functionalities are implemented to interact with elements on the web page and track user interactions. Here's a description of the key approaches and actions performed within the script:

Initialize an Array (arr): An array named arr is created to store information about selected elements.

# selectButton(buttonNumber):
This function is responsible for handling interactions with buttons and the video element.
It takes a buttonNumber parameter to identify which button was clicked.
If the clicked button is the video button (with buttonNumber 4), it adds a "video-border" class to highlight it.
It checks if the selected element does not already have the "selected" class. If not, it adds the "selected" class to the element and records interaction details (element type, label) in the arr array.
If the element already has the "selected" class, it removes the "selected" class, the "video-border" class (if it's a video), and attempts to remove an element from the arr array. However, there's an issue in the arr manipulation: arr should be spliced instead of assigning the result back to arr.

It checks if the clicked element has the "selected" class, indicating a selected element.
If the element is selected, it logs the interaction details (element type, label) to the console.

# Initialize Dashboard Elements:
The script sets up a dashboard section in the HTML (#dashboard) to display the recorded interactions.
It initializes an empty unordered list (ul) for this purpose.

# Track and Update Interactions:
Another document.addEventListener('click') event listener is set up to track interactions.
If a selected element is clicked, it captures its element type and label.
It creates a unique key for this interaction based on element type and label.
It maintains a count of interactions for each unique key in the interactionCounts object.
It logs the interaction details and updates the dashboard with the latest interaction counts.

# updateDashboard():
This function is responsible for updating the dashboard with the recorded interactions.
It clears the existing content of the dashboard list.
It iterates through the interactionCounts object and creates list items for each unique interaction, displaying the element type, label, and interaction count.

