# Configuration Guide for Home Classroom Integration
---

Welcome to the Home Classroom Integration! This page will walk you through the simple steps to get the integration up and running in Home Assistant.

Step 1: Set Up Google Cloud Console

Before you can use this integration, you need to create a project in Google Cloud and set up OAuth2 to connect your Google account to the integration.

    Create a Google Cloud Project:
        Go to Google Cloud Console.
        Click on Select a Project at the top, then click New Project.
        Give your project a name, then click Create.

    Enable Google Classroom API:
        In the Google Cloud Console, go to API & Services > Library.
        Search for Google Classroom API and click on it.
        Click Enable to turn on the Google Classroom API for your project.

    Set Up OAuth2 Credentials:
        In the Google Cloud Console, go to API & Services > Credentials.
        Click Create Credentials, then select OAuth 2.0 Client ID.
        You may be prompted to configure the OAuth consent screen. Fill in the required fields (you can leave them simple since this is just for personal use or an open-source project).
        Under Application Type, select Web Application.
        For the Authorized redirect URIs, enter the Home Assistant redirect URI (this will be provided in the Home Assistant setup process).
        Click Create, and make note of your Client ID and Client Secret.

Step 2: Install the Home Classroom Integration in Home Assistant

    Install Dependencies:
        Open a terminal or command prompt and run the following command to install the required Python libraries:

    pip install --upgrade pip
    pip install homeassistant google-auth google-auth-oauthlib google-auth-httplib2 google-api-python-client requests

Configure the Integration in configuration.yaml:

    In your Home Assistant configuration folder, open the configuration.yaml file.
    Add the following to your configuration.yaml file:

        homeclassroom:
          client_id: YOUR_GOOGLE_OAUTH2_CLIENT_ID
          client_secret: YOUR_GOOGLE_OAUTH2_CLIENT_SECRET
          project_id: YOUR_GOOGLE_PROJECT_ID

        Replace the placeholders (YOUR_GOOGLE_OAUTH2_CLIENT_ID, YOUR_GOOGLE_OAUTH2_CLIENT_SECRET, and YOUR_GOOGLE_PROJECT_ID) with the credentials you created in the Google Cloud Console.

Step 3: Authenticate with Your Google Account

    Restart Home Assistant:
        After updating your configuration.yaml file, restart Home Assistant to apply the changes.

    Sign In with Your Google Account:
        When you restart Home Assistant, you’ll be prompted to authenticate with your Google account.
        Click the link in the prompt, and log in with your Google account that is connected to Google Classroom.
        Allow the integration access to your Google Classroom data (assignments and homework).

Step 4: Enjoy Assignment Updates

Once authenticated, the integration will start pulling assignment data from Google Classroom, such as:

    Assignment names
    Due dates
    Status of the assignments

You will receive notifications and updates directly within Home Assistant.
Optional: Advanced Configuration (Optional)

If you want to tweak settings or change notification behaviors, you can modify the integration settings in Home Assistant. Refer to the Home Assistant documentation for advanced setup or troubleshooting.
Troubleshooting

If something isn’t working, check the following:

    OAuth2 Authentication: Make sure you’ve entered your Google OAuth2 credentials correctly.
    API Access: Double-check that the Google Classroom API is enabled in the Google Cloud Console.
    Logs: Look at the Home Assistant logs for error messages if there are issues with the integration.

That’s it! You’ve now set up the Home Classroom Integration to keep track of your assignments and homework in Home Assistant.