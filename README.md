# cdc-uploading-tool

This is a Flask-based web application designed as a plugin for SAP Customer Data Cloud (CDC), offering additional features.

## Table of Contents
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Screenshots](#screenshots)
- [License](#license)


## Setup Instructions

After cloning the repository, follow these steps to set up the project:

1. **Set up local environment**:
   - Download and install JetBrains PyCharm IDE or your preferred IDE.
   - The following instructions will focus on PyCharm, but most IDEs provide similar features.

2. **Open the project**:
   - In PyCharm, navigate to `File -> Open` and select the cloned repository folder.

3. **Set Up a local virtual environment**:
   - Go to `Settings` > `Project: finance-gpt` > `Python Interpreter` > `Add Interpreter`.
   - Choose `Add Local Interpreter` > `Virtualenv Environment`.
     1. Select `Environment` -> `New`.
     2. Set `Base Interpreter` to your installed Python version (e.g., Python 3.x).
     3. Click `OK`.

4. **Install dependencies**:
   - Install required dependencies by running the following command in terminal through IDE:
     ```bash
     pip install -r requirements.txt
     ```
   - If AI language translation is required through SAP Gen AI Hub, run following command:
     ```bash
     pip install "generative-ai-hub-sdk[all]==1.2.2" --extra-index-url https://int.repositories.cloud.sap/artifactory/api/pypi/proxy-deploy-releases-hyperspace-pypi/simple/
     ```
   - If you prefer to connect directly to the LLM via OpenAI instead of using the SAP proxy, you can skip the installation of `generative-ai-hub-sdk` and install required LangChain libraries instead.

5. **Local configuration setup**:
   In properties.yml, set SAP Gen AI hub credentials or OpenAI key (if AI based language translation is required)

6. **Run the Application**:
   ```bash
   python app.py
   ```
  
7. **Access the user interface**:
Open your web browser and navigate to [http://localhost:5001/](http://localhost:5001/) (or the appropriate port if different).

## Usage
Once the application is running, you can use various features from interactive UI.

## Screenshots
Here are some screenshots showcasing working deployments of the application.
- Home page:
  <img width="1728" alt="1_home" src="https://github.com/user-attachments/assets/81585e8e-59af-4a93-916e-c961713eb2c4" />

- Set configuration credentials:
  <img width="1727" alt="2_config" src="https://github.com/user-attachments/assets/7c81d95c-437c-413f-922f-fe894e5df98a" />

- Filled template downloaded from _Template Creation_ page:
  <img width="1510" alt="3_filled_template" src="https://github.com/user-attachments/assets/44a87b15-97c8-4501-a598-55fd27d6d44e" />

- _Upload Excel_ page:
  <img width="1720" alt="4_upload" src="https://github.com/user-attachments/assets/e7cd8ee0-cf9a-483a-8d5c-abceb6a51922" />

- Response for uploaded data, with success as well as error scenarios:
  <img width="1728" alt="5_upload_response" src="https://github.com/user-attachments/assets/759bb868-b6c7-4adb-8168-26f9e66ac4cd" />

- Excel exported for upload response data:
  <img width="1509" alt="6_response_export" src="https://github.com/user-attachments/assets/a4eafd8c-fa1d-408f-9997-576dad7ced9f" />

- Generative AI based language translation:
  <img width="1728" alt="7_ai_translate" src="https://github.com/user-attachments/assets/70d9c1bc-71a4-4acb-8971-443ae41fb5d7" />


## License
This project is licensed under the MIT License. See the LICENSE file for more details.
