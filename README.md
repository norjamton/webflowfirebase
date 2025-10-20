# Webflow Firebase Template

Template for hosting Webflow sites on Firebase with automated sync scripts.

## Setup

1. Replace placeholders in configuration files:
   - In `.firebaserc`: Replace `${FIREBASE_PROJECT_ID}` with your Firebase project ID
   - In `package.json`: Replace `${WEBFLOW_SITE_ID}` with your Webflow site ID (found in your site URL: `https://[site-id].webflow.io`)

2. Install Firebase CLI if not already installed:
   ```bash
   npm install -g firebase-tools
   ```

3. Login to Firebase:
   ```bash
   firebase login
   ```

4. Initialize the project:
   ```bash
   npm install
   ```

## Available Scripts

- `npm run pull-webflow`: Pulls the latest version of your site from Webflow
- `npm run push-github`: Pushes changes to GitHub with "Sync with webflow" message
- `npm run sync`: Runs pull-webflow, push-github, and firebase deploy in sequence

## Important Notes

⚠️ When making local changes:
- There is no automated way to import local changes back into Webflow
- Make changes in Webflow first, then sync them to this repo
- Use this repo primarily for:
  - Code inspection
  - Version control
  - Firebase hosting
  - Backup purposes

## Customization

You can modify the scripts in `package.json` to add additional functionality or change the default commit messages as needed.