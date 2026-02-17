<img width="1024" height="796" alt="image" src="https://github.com/user-attachments/assets/fc432e78-d88c-463b-97b9-7f4217ad5c0d" />


# Workspace Replicator for Google Drive

A professional-grade **Google Apps Script (GAS)** application designed to standardize project onboarding. This tool provides a structured, five-step wizard for replicating complex folder hierarchies from a user's Drive root or a specific Folder ID into a new, validated instance.

---

## Key Functionalities

### Advanced Source Discovery
* **Root Directory Integration**: Automatically scans the user's Google Drive root to populate the initial selection list.
* **Dynamic Subfolder Navigation**: Includes a cascading dropdown system that fetches sub-directories in real-time once a parent folder is selected.
* **Manual Identifier Support**: Allows for the direct input of a Folder ID to clone templates shared from external sources or deep-directory structures.

### Verification and Safety
* **Live Preview Engine**: Accesses the source template to display a subset of its contents (files and subfolders) before replication begins.
* **Recursive Cloning**: Utilizes a deep-copy algorithm to ensure all nested assets and folder structures are preserved in the destination.

### User Experience
* **Haptic Audio Feedback**: Uses the **Web Audio API** to generate a localized, low-volume mechanical click for primary navigation actions.
* **SPA Architecture**: Managed as a Single Page Application to ensure fast transitions without full-page browser reloads.
* **Persistent State Management**: Maintains user selections across the wizard, allowing for easy "Back" navigation and data validation.

---

## Technical Specifications

| Component | Technology |
| :--- | :--- |
| **Backend Environment** | Google Apps Script (V8 Engine) |
| **User Interface** | HTML5, CSS3 (Custom Properties), JavaScript (ES6+) |
| **Google APIs** | DriveApp (Native GAS Service) |
| **Audio Processing** | Web Audio API (Triangle Oscillator) |
| **Typography** | Inter (Standard Enterprise Sans-Serif) |

---

## Installation and Deployment

### Script Setup
1. Open the [Google Apps Script Dashboard](https://script.google.com).
2. Create a new project and replace the contents of `Code.gs` with the provided application code.
3. Save the project with a descriptive name.

### Web App Configuration
1. Navigate to **Deploy** > **New Deployment**.
2. Select **Web App** as the deployment type.
3. Set the following configurations:
   * **Execute as**: Me (your account)
   * **Who has access**: Anyone with a Google account (or restricted to your Workspace domain)
4. Copy the generated **Web App URL** for distribution.

---

## Operational Workflow

1. **Step 1: Source Identification**: Choose between browsing the root Drive or entering a specific ID. A secondary dropdown appears for subfolder selection.
2. **Step 3: Resource Naming**: Provide a unique name for the new folder. Validation ensures the "Next" button remains disabled until a name is entered.
3. **Step 3: Audit and Preview**: The system fetches the template structure for user review to confirm the correct project environment.
4. **Step 4: System Replication**: The backend initiates the `copyRecursive` process. A visual spinner is displayed during this high-latency operation.
5. **Step 5: Provisioning Complete**: A confirmation screen provides a direct link to the new folder. The "Create Another Instance" option allows for a full state reset.

---

## Security and Compliance
* **Organization-Centric**: Respects existing Google Workspace Drive permissions and Data Loss Prevention (DLP) policies.
* **Zero-Data Storage**: The application does not store information on external databases; all operations are performed directly within the Google ecosystem.
* **Scoped Access**: The script only interacts with data the authenticated user has explicit permissions to access.

---

## License
This project is licensed under the MIT License.
