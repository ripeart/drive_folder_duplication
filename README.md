<img width="1151" height="634" alt="image" src="https://github.com/user-attachments/assets/26b62433-a49c-4bc3-93f9-a580e7c26c4b" />


# Google Drive Folder Template Copier

A modern, glassmorphic web application built with Google Apps Script. This tool allows users to select a directory structure from a central Templates folder and clone it directly into their own Google Drive with a custom name.

---

## Features

* **Dynamic Template Discovery**: Automatically scans a specific Google Drive folder for subfolders to use as templates.
* **Searchable Dropdown**: Powered by Choices.js for quick filtering of template lists.
* **Safety Validation**: Built-in Regex validation to prevent illegal characters in Google Drive folder names.
* **Premium UI**: A high-end dark mode interface featuring frosted glass effects, mesh gradients, and smooth animations.
* **User-Centric Execution**: Clones folders directly into the My Drive of the user accessing the app.

---

## Deployment Guide

### 1. Prepare your Templates
1. Create a folder in Google Drive to hold all your templates.
2. Each subfolder inside this Master folder will appear as an option in the app dropdown menu.
3. **Important**: Share this Master folder with your organization with at least **Viewer** access.
4. Copy the Folder ID from the URL (the string of characters after `folders/`).

### 2. Setup the Script
1. Go to the [Google Apps Script dashboard](https://script.google.com) and create a New Project.
2. Paste the code from `Code.gs` into the editor.
3. Replace the `MASTER_TEMPLATES_FOLDER_ID` constant at the top with your Folder ID:
   ```javascript
   const MASTER_TEMPLATES_FOLDER_ID = 'YOUR_FOLDER_ID_HERE';
