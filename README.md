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
  <img width="1728" alt="1_home" src="https://github.com/user-attachments/assets/80b97d9a-edb5-42c8-ac18-2409e10cc7b8" />

- Set configuration credentials:
  <img width="1727" alt="2_config" src="https://github.com/user-attachments/assets/6ba0846d-f89e-4608-8c3f-3ccf2a74a42f" />

- Filled template downloaded from _Template Creation_ page:
  <img width="1510" alt="3_filled_template" src="https://github.com/user-attachments/assets/e2b1cf4c-9a17-48ca-b627-e60fabd0a4f0" />

- _Upload Excel_ page:
  <img width="1720" alt="4_upload" src="https://github.com/user-attachments/assets/4afb208e-fec5-4281-9dcb-a96478ef9002" />

- Response for uploaded data, with success as well as error scenarios:
  <img width="1728" alt="5_upload_response" src="https://github.com/user-attachments/assets/5ecd9171-7f8d-4019-b2ce-0bd1521fd695" />

- Excel exported for upload response data:
  <img width="1509" alt="6_response_export" src="https://github.com/user-attachments/assets/53b28d17-a1ca-421c-9f9b-2295e9d446dc" />

- Generative AI based language translation:
  <img width="1728" alt="7_ai_translate" src="https://github.com/user-attachments/assets/ddd57cc6-8222-40f2-bdfa-c0475bc8f653" />


## License
This project is licensed under the MIT License. See the LICENSE file for more details.
