<img width="970" height="676" alt="image" src="https://github.com/user-attachments/assets/1d2bd8e0-7218-4e27-90ce-dcc558199044" />

📂 Enterprise Workspace Replicator
A high-performance Google Apps Script (GAS) web application designed for standardized project onboarding. This tool allows users to replicate complex folder structures from their Google Drive root or a specific Folder ID into a new, named instance with a streamlined, multi-step wizard interface.

✨ Features
5-Step Enterprise Wizard: Guided process including Source Selection, Project Details, Content Preview, Replication, and Success confirmation.

Dynamic Source Selection:

Root Drive Explorer: Automatically fetches folders from the user's Drive root.

Subfolder Navigation: Cascading dropdowns allow users to drill down into a specific parent folder to select a template.

Folder ID Entry: Support for manual ID input for shared or deep-directory templates.

Live Content Preview: Fetches a real-time list of files and folders within the source template to ensure accuracy before cloning.

Recursive Replication Engine: Deep-copies all files and subdirectories while maintaining the original structure.

Haptic Audio Feedback: Integration of the Web Audio API to generate a quiet, professional mechanical "click" on primary actions without external dependencies.

State-Driven UI: A single-page application (SPA) feel using CSS transitions and JavaScript state management to prevent browser reloads.

🚀 Tech Stack
Backend: Google Apps Script (V8 Engine)

Frontend: HTML5, CSS3 (Flexbox/Grid), JavaScript (ES6+)

APIs: Google Drive API, Web Audio API

Typography: Inter (via Google Fonts)

🛠️ Installation & Setup
Create a New Project:

Go to script.google.com and create a new project.

Add the Code:

Copy the contents of Code.gs from this repository into the script editor.

Deploy as Web App:

Click Deploy > New Deployment.

Select Web App.

Set Execute as: Me.

Set Who has access: Anyone within [Your Organization] (or Anyone for public use).

Authorize:

Grant the necessary permissions to access your Google Drive when prompted.

📖 Usage
Step 1 (Source): Choose to browse your root Drive or paste a specific Folder ID. If browsing, select a parent and optionally a subfolder.

Step 2 (Details): Enter the name for your new workspace instance.

Step 3 (Preview): Verify the files listed are the correct template assets.

Step 4 (Copying): Wait for the system to synchronize and replicate the directory.

Step 5 (Success): Open your new folder directly via the generated link or reset the wizard to create another instance.

🔒 Security & Privacy
No Data Storage: This application does not store user data. It acts as a bridge between the source and destination folders within the user's own Google Drive.

Authorization: The script only accesses folders the user has explicit permission to view or edit.

📄 License
Distributed under the MIT License. See LICENSE for more information.
