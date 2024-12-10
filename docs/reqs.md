# Requirements for Home Classroom Integration
---

To use the Home Classroom Integration with Home Assistant, you’ll need to make sure you have the following requirements in place:
1. Home Assistant

    This integration is designed to work with Home Assistant. You can install Home Assistant on various platforms (e.g., Raspberry Pi, Docker, Virtual Machine). Follow the Home Assistant installation guide to get it set up.

2. Google Account

    You’ll need a Google Account to connect to Google Classroom via OAuth2.
    The integration pulls your assignment data from Google Classroom.

3. Google Cloud Console Setup

Before you can authenticate, you'll need to set up a project in the Google Cloud Console:


4. Home Assistant Installation for Development (Optional)

If you want to contribute to the project or test the integration locally:

    Python: Ensure that you have Python 3.9 or later installed. Use a virtual environment for isolating dependencies.
    Home Assistant Core: You can install Home Assistant Core on your local machine using:

    pip install homeassistant

5. Dependencies

The integration uses several Python libraries. 

Here are the key dependencies:

    homeassistant: Required to interact with Home Assistant and manage integrations.
    google-auth: Handles OAuth2 authentication for Google services.
    google-auth-oauthlib: OAuth2 library for easier Google account authentication.
    google-api-python-client: The official client library for interacting with Google APIs, including Google Classroom.
    requests: For making HTTP requests to Google’s servers and handling API calls.

6. Optional - Developer Tools (For Contributing)

If you want to contribute or modify the integration, you’ll need the following developer tools:

    Docker: For running Home Assistant in a container (optional).
    Visual Studio Code: A popular code editor to make changes and test the integration locally.
    Home Assistant Development Tools: Follow the Home Assistant developer docs to set up your development environment.