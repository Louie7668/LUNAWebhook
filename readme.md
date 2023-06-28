# GitHub Webhook Discord Integration

Made by kerfoot on discord

This project allows you to integrate GitHub webhooks with Discord using Node.js and the discord-webhook-node library. Whenever a webhook event is triggered on a GitHub repository, a corresponding message will be sent to a specified Discord channel.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Customization](#customization)
- [Limitations](#limitations)
- [Troubleshooting](#troubleshooting)
- [License](#license)

## Prerequisites

Before using this project, make sure you have the following prerequisites installed:

- Node.js (version 12 or above)
- npm (Node Package Manager)

## Getting Started

To get started with the GitHub webhook Discord integration, follow these steps:

1. Clone the repository to your local machine:

```git clone https://github.com/your-username/github-webhook-discord-integration.git```

2. Navigate to the project directory:

```cd github-webhook-discord-integration```

3. Install the dependencies using npm:

```npm install```

4. Configure the webhook URL:

- Open the `config.js` file in a text editor.
- Replace the value of `config.webhook` with the URL of your Discord webhook. You can create a webhook in your Discord server settings.


5. Start the application:

```npm run start```

This will start the Node.js server and listen for incoming GitHub webhook events.

6. Configure the GitHub repository webhook:

- Open your GitHub repository in a web browser.
- Go to **Settings** -> **Webhooks** -> **Add webhook**.
- In the **Payload URL** field, enter the URL of your Node.js server where the application is running (`http://your-server-ip:your-port/recieve_github`).
- Select the events you want to trigger the webhook (e.g., push, pull request, etc.).
- Save the webhook configuration.

7. Testing the integration:

- Make changes to your GitHub repository that trigger the configured webhook events (e.g., push a new commit).
- Check the Discord channel specified in the webhook URL. You should see messages corresponding to the triggered events.

## Using Commits and Descriptions
When making commits to your GitHub repository, you can use a specific format for the commit message to generate formatted messages in the Discord channel. The recommended format is as follows:

Title: <type>(<scope>): <subject>

Description: <description>

<type>: Describes the type of change (e.g., feat, fix, docs, style, refactor, test, chore, etc.).
<scope> (optional): Describes the scope of the change (e.g., files, server, client, etc.).
<subject>: Briefly summarizes the change.
<description> (optional): Provides a detailed description of the change.

For example, a commit message could be:

```Title: tweak(files): added bank heist```

```Description: Added server and client-side bank heist. Tweaked the server script.```


## Customization

- You can customize the messages sent to Discord by modifying the code in the `app.post('/recieve_github')` route in `index.js`. Update the message formats, colors, and other properties based on your preference.

## Limitations

- The maximum file size limit for pushing files is set to 2GB by default. You can adjust this limit by modifying the `app.use(bodyParser.json({ limit: '2000mb' }))` line in `index.js`.

## Troubleshooting

- If you encounter any issues or errors, ensure that you have correctly followed the steps above and that all dependencies are properly installed.

## License

This project is licensed under the [MIT License](LICENSE).

