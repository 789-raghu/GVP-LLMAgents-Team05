# GVP-LLMAgents-Team05 Documentation

## Opening the Application
To set up and run the application, follow these steps:

1. Install the necessary dependencies by running:
   ```sh
   pip install streamlit PyPDF2 python-dotenv
   ```
2. Launch the application with:
   ```sh
   streamlit run job_description.py
   ```

---

## Prerequisites
Before proceeding, ensure you have the following:

- **OpenAI API Key** - Required for AI-based functionalities.
- **Gmail App Password** - Generate an App Password for secure email sending.
- **Access to Google Cloud Console** - Necessary for enabling APIs and managing credentials.

---

## Google Cloud Console Setup
To enable the necessary services and configure credentials, follow these steps:

1. Navigate to [Google Cloud Console](https://console.cloud.google.com/).
2. Enable **Google Forms API** and **Google Drive API** by searching for them in the "Enabled APIs & Services" section.
3. Create a **new project** in Google Cloud Console.
4. Set up the **OAuth Consent Screen** and configure it for your application.
5. Go to **Credentials** and create a **Service Account**:
   - After creating the account, generate a new **Key** and download it as a JSON file.
   - Add this JSON key file to your project repository.

---

## Question and Form Generation
To generate Google Forms-based assessments, follow these steps:

1. Install the required libraries from `requirements.txt`:
   ```sh
   pip install -r requirements.txt
   ```
2. Navigate to `send_assessment.py` and make necessary modifications:
   - Set the path of `service_account.json`.
   - Enter your **OpenAI API Key**.
   - Add the **authorized email** that can edit and view responses.
3. Run the script to generate the Google Form:
   ```sh
   streamlit run send_assessment.py
   ```
4. A Google Form will be created along with a text file containing the questions and correct answers.
5. From the **authorized email**, access the Google Form:
   - Enable **Quiz Mode**.
   - Manually select correct answers from the generated text file.
   - Assign marks to the questions.
6. Share the quiz link with the participants.

---

## Extraction and Email Generation
To evaluate participant responses and send emails to qualified candidates:

1. Copy the link of the **Google Sheets** associated with the Google Form.
2. Add the spreadsheet to your project repository.
3. Update the `.env` file:
   - Set the correct **spreadsheet path**.
   - Enter the **Gmail address** and **Gmail App Password**.
4. Run the performance evaluation script:
   ```sh
   streamlit run evaluate_performance.py
   ```
5. The system will automatically send emails to qualified candidates based on their performance.

---

## Conclusion
By following the above steps, you can:
- Generate AI-powered assessments.
- Automate quiz distribution and evaluation.
- Efficiently notify qualified candidates via email.

This documentation ensures a smooth setup and execution of the **GVP-LLMAgents-Team05** system. For any troubleshooting, refer to the respective sections or consult the project team.
