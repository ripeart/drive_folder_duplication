Google Drive Folder Template Copier
A modern, glassmorphic web application built with Google Apps Script. This tool allows users to select a directory structure from a central Templates folder and clone it directly into their own Google Drive with a custom name.

Features
Dynamic Template Discovery: Automatically scans a specific Google Drive folder for subfolders to use as templates.

Searchable Dropdown: Powered by Choices.js for quick filtering of template lists.

Safety Validation: Built-in Regex validation to prevent illegal characters in Google Drive folder names.

Premium UI: A high-end dark mode interface featuring frosted glass effects, mesh gradients, and smooth animations.

User-Centric Execution: Clones folders directly into the My Drive of the user accessing the app.

Deployment Guide
1. Prepare your Templates
Create a folder in Google Drive to hold all your templates.

Each subfolder inside this Master folder will appear as an option in the app dropdown menu.

Important: Share this Master folder with your organization with at least Viewer access.

Copy the Folder ID from the URL (the string of characters after folders/).

2. Setup the Script
Go to the Google Apps Script dashboard and create a New Project.

Paste the code from Code.gs into the editor.

Replace the MASTER_TEMPLATES_FOLDER_ID constant at the top with your Folder ID:

JavaScript

const MASTER_TEMPLATES_FOLDER_ID = 'YOUR_FOLDER_ID_HERE';
Name your project (e.g., "Organization Template Tool").

3. Deploy as a Web App
Click Deploy and select New deployment.

Select Web app as the deployment type.

Configure the following settings:

Execute as: User accessing the web app. This ensures the copy is created in the user's Drive.

Who has access: Anyone within your organization.

Click Deploy and copy the Web App URL.

Technical Details
Dependencies
Google Apps Script: Manages the backend DriveApp interactions.

Choices.js: Provides the searchable, stylized dropdown menu.

Inter Font Family: Sourced via Google Fonts for modern typography.

Validation Logic
The app rejects folder names containing the following characters to ensure compatibility across all Google Drive integrations: / \ : * ? " < > |

Instructions for Use
Navigate to the Web App URL.

Search for the template you wish to copy from the dropdown.

Enter a valid name for the new folder.

Select Create Copy in My Drive.

Once the process is finished, select the Open Folder button to go directly to the new workspace in Google Drive.

License
Distributed under the MIT License.
