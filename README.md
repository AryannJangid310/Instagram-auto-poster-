# Insta Auto Poster 📸

A powerful Node.js automation tool that posts images to Instagram using Puppeteer. It handles the full workflow including login, popup management, and posting with captions.

## Features

- **Automated Login**: Securely logs in using provided credentials.
- **Smart Popup Handling**: Automatically dimisses "Save Info", "Not Now", and new "Messaging" popups.
- **Full Posting Workflow**:
  - Creates new post
  - Uploads image (via file input simulation)
  - Handles cropping and filter screens
  - Adds caption
  - Shares the post
- **Robust Navigation**: Uses retry logic to ensure stability against network lag.

## Prerequisites

- Node.js (v14 or higher)
- Google Chrome (optional, Puppeteer installs Chromium)

## Installation

1.  Clone the repository:
    ```bash
    git clone https://github.com/yourusername/insta-auto-poster.git
    cd insta-auto-poster
    ```

2.  Install dependencies:
    ```bash
    npm install
    ```

## Configuration

1.  Navigate to the config directory:
    ```bash
    cd src/config
    ```

2.  Create your configuration file from the example:
    - Copy `config.example.js` to `config.js`
    - **Important**: `config.js` is gitignored to keep your credentials safe.

3.  Edit `src/config/config.js` with your Instagram credentials:
    ```javascript
    module.exports = {
      instagram: {
        username: 'your_username',
        password: 'your_password'
      },
      // Optional: Set a default caption in config
      caption: 'My wonderful post!',
      // ...
    };
    ```

## Usage

1.  Place the image you want to post in a known location (or update the path in `src/index.js`).

2.  Run the script:
    ```bash
    node src/index.js
    ```

## Project Structure

- `src/index.js`: Main entry point.
- `src/modules/instagram.js`: Login and popup handling logic.
- `src/modules/instagram_post.js`: Core posting workflow logic.
- `src/config/`: Configuration files.

## Disclaimer

This tool is for educational purposes only. Automated scraping or posting may violate Instagram's Terms of Service. Use responsibly.

## License

MIT
