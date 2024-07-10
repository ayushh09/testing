# Proof of Concept (POC) for Slack Notifications in Jenkins
| Created/Updated | Version  | Author | Comment |
|:---------------:|:--------:|:------:|:-------:|
| 24-06-2024      | 1.0 | Naresh Boyini | Initial documentation |
## Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
  - [Generate an API Token](#generate-an-api-token)
  - [Install and Configure the Slack Plugin in Jenkins](#install-and-configure-the-slack-plugin-in-jenkins)
  - [Configure a Jenkins Job to Send Slack Notifications](#configure-a-jenkins-job-to-send-slack-notifications)
- [Testing the Setup](#testing-the-setup)
- [Conclusion](#Conclusion)
- [Contact Information](#contact-information)
- [References](#references)
## Introduction
This document outlines the prerequisites, step-by-step guide, and contact information for setting up Slack notifications in Jenkins.Integrating Slack with Jenkins enables real-time build notifications, enhancing collaboration and efficiency in the development workflow.
## Prerequisites
Before you begin, ensure you have the following:
- **Slack Account and Workspace**: A Slack workspace where you can create a channel for Jenkins notifications.
- **Jenkins Server**: A Jenkins server up and running.
- **Slack Plugin for Jenkins**: The Slack Notification Plugin installed in Jenkins.
## Getting Started
### Steps
### 1. Generate an API Token
1. **Create a Slack App**:
    - Go to the App in Slack.
    - Search for 'Jenkins CI'.
![step-00](https://github.com/mygurkulam-p9/documentation/assets/160397679/76af9144-aa95-4942-9ffc-f14d0f0571a9)
    - Click on "Add to Slack".
    - choose the channel where you want to post notifications.
    - Click "Add Jenkins CI Integration".
![step-01](https://github.com/mygurkulam-p9/documentation/assets/160397679/8c951e1c-f376-4130-b759-5bc8fd839057)
2. **Follow the Setup instructions that will be provided**:
   - Copy the integration token credential ID and securely store it..
![setup-introcutions](https://github.com/mygurkulam-p9/documentation/assets/160397679/45fb23c0-247d-4aec-82d9-cd068d0645cb)
3. **Save the settings**
![save-settings](https://github.com/mygurkulam-p9/documentation/assets/160397679/10b4e282-d9b5-4801-ad8d-9f1a26891e8b)
### 2. Install and Configure the Slack Plugin in Jenkins
1. **Install the Plugin**:
    - Go to your Jenkins dashboard.
    - Navigate to "Manage Jenkins" > "Manage Plugins".
    - In the "Available" tab, search for "Slack Notification Plugin".
    - Select it and click "Install without restart".
![step-02](https://github.com/mygurkulam-p9/documentation/assets/160397679/3729620a-b390-42f7-b4aa-b4b5fb262e73)
2. **Configure the Slack Plugin**:
    - After installation, go to "Manage Jenkins" > "Configure System".
    - Scroll down to the "Slack" section.
    - Fill in the following details:
        - **Workspace**: Enter your Slack workspace domain.
        - **Credential**: Add a new credential of type "Secret text" with the Slack API token generated earlier.
        - **Default Channel**: Enter the default channel name.
![step-03](https://github.com/mygurkulam-p9/documentation/assets/160397679/842ccc8f-1ee9-48a4-b22e-dc81b98ccb42)
### 3. Configure a Jenkins Job to Send Slack Notifications
1. **Create or Edit a Jenkins Job**:
    - Go to the job you want to configure Slack notifications for.
    - Click "Configure".
2. **Post-Build Actions**:
    - Scroll down to the "Post-build Actions" section.
    - Click on "Add post-build action" and select "Slack Notifications".
3. **Configure Notifications**:
    - Choose when to send notifications (e.g., "Notify Success", "Notify Failure").
    - Optionally, you can specify a different Slack channel for this job.
4. **Save the Configuration**:
    - Click "Save".
![step-06](https://github.com/mygurkulam-p9/documentation/assets/160397679/1a34037e-8758-49bc-a1c5-826d76906b0b)
### Testing the Setup
1. **Run a Build**:
    - Trigger a build for the configured job.
    - Check the Slack channel for notifications.
![step-04](https://github.com/mygurkulam-p9/documentation/assets/160397679/e50d322f-431a-4478-ace7-e3c765ff2ffc)
![step-05](https://github.com/mygurkulam-p9/documentation/assets/160397679/b96e3c16-af93-4239-952c-a201a1437fe4)
### Notification with Different Users
![jenkins-diff-users](https://github.com/mygurkulam-p9/documentation/assets/160397679/fcb67e42-b62d-4ce9-a2c9-30c64a77594c)
2. **Troubleshooting**:
    - If notifications are not appearing, check the Jenkins logs for any errors.
    - Ensure the Slack API token is valid and the app has the necessary permissions.
## Conclusion
This Document outlines the steps to set up the integration, including generating an API token, installing and configuring the Slack plugin in Jenkins, and setting up notifications for specific jobs. Following these steps ensures your team stays informed and can respond quickly to build results, improving collaboration and productivity.
## Contact Information
|NAME|	Email Address|
|----|---------------|
|Naresh Boyini| naresh.boyini.snaatak@mygurukulam.co|
## References
| Resource                                    | Link                                                  |
|---------------------------------------------|-------------------------------------------------------|
| Jenkins Documentation                       | [Jenkins Documentation](https://www.jenkins.io/doc/)  |
| Slack API Documentation                     | [Slack API Documentation](https://api.slack.com/)     |
| Slack Notification Plugin for Jenkins       | [Slack Notification Plugin](https://plugins.jenkins.io/slack/) |
| Continuous Integration with Jenkins         | [Continuous Integration with Jenkins](https://www.jenkins.io/doc/book/pipeline/jenkinsfile/) |
| Slack API: Applications                     | [Slack API: Applications](https://api.slack.com/apps) |
