📸 Alpha V Pro Photo Booth Deployment Guide

Follow this guide to host your professional, serverless glassmorphism Photo Booth on GitHub Pages, connecting your Lenovo tablet and DJI Osmo Nano securely to Google Drive.

🏗️ Step 1: Push Code to GitHub

Create a new public repository on your GitHub account (e.g., photobooth or inside your alvarias.github.io portfolio repo).

Save the complete index.html file into the root of this repository.

Commit and push the files.

🌐 Step 2: Enable GitHub Pages Hosting

In your GitHub repository, navigate to the Settings tab.

Select Pages from the sidebar menu.

Under the "Build and deployment" configuration, make sure the Source is set to Deploy from a branch.

Choose main (or master) and folder path /root, then click Save.

Wait roughly a minute. Your secure URL will be published at the top of the section (e.g., https://yourusername.github.io/photobooth/).

🔑 Step 3: Configure Google Cloud Credentials

Google requires a quick security configuration to authorize your web app browser window to write files safely to your Google Drive.

Go to the Google Cloud Console.

Click the project dropdown at the top left and select New Project. Name it Alpha-V-PhotoBooth.

Search for the Google Drive API in the top search box and click Enable.

Go to the OAuth consent screen tab:

Select External as User Type.

Enter your support email addresses.

Click Scopes, search for and add https://www.googleapis.com/auth/drive.file. This ensures your app only has permissions to edit and write files it created, locking access to your rest of Drive.

Add your own Google Account email to the Test Users panel (this lets you test without official Google review).

Generate security keys under the Credentials tab:

Select + Create Credentials > API Key. Copy this key.

Select + Create Credentials > OAuth client ID > Select Web application.

Under Authorized JavaScript origins, add your GitHub URL (e.g., https://yourusername.github.io).

Under Authorized redirect URIs, add your exact published Page URL (e.g., https://yourusername.github.io/photobooth/).

Copy your generated Client ID.

📁 Step 4: Arrange Google Drive Folders

Create two separate folders in your Google Drive:

Folder 1: RAW Captures (For original, un-framed photos).

Folder 2: FRAMED Outputs (For the compiled frames and strips).

Open each folder on your computer's browser. Look at the address bar URL. The long string of letters and numbers at the end of the link is the unique Folder ID! Keep these IDs handy.

🔌 Step 5: Arrange Hardware & Run the App

Connect a multi-port USB-C Hub with Power Delivery (PD) to your Lenovo tablet.

Plug your tablet's charger cable into the Hub's PD port (verifying the tablet shows "Charging").

Set your DJI Osmo Nano to Webcam/UVC mode in its hardware options.

Plug the DJI camera into a USB Data port on the Hub.

Open Chrome on your tablet and navigate to your live GitHub Pages URL.

The setup dashboard will appear:

Paste your Client ID and API Key.

Enter your Event Name.

Paste both Folder IDs.

Select your DJI camera input device from the drop-down menu!

Upload your custom assets (or leave blank to use the built-in golden vector frames).

Click Initialize Photobooth Terminal, authorize Google permissions when prompted, and start the booth! 🎉
