# Ye Olde Hangout Scroll

A multiplayer, medieval-themed web app for friends to collaboratively decide on activities. Add your ideas to a shared scroll and let fate (a random wheel spinner) decide what you do next! The entire application is a single, self-contained HTML file that uses Firebase for real-time database and authentication.

![Screenshot of Ye Olde Hangout Scroll](https://i.imgur.com/rG7nZ7a.png)

## Features

- **Real-time Collaboration:** Add ideas to a shared list that updates instantly for all users.
- **Themed Interface:** A beautiful, manuscript-style design with medieval fonts, textures, and a "Wheel of Fortune" spinner.
- **Random Idea Picker:** Click the illustrated wheel to randomly select an activity from the pool.
- **Avoid Repeats:** An option to ensure that once an idea is picked, it won't be picked again until you "cleanse the slate."
- **Persistent Storage:** Your list of ideas is saved in a Firebase Firestore database.
- **Serverless:** No backend server to manage. The entire app runs in the browser and connects directly to Firebase services.

## Tech Stack

- **Frontend:** HTML, Tailwind CSS
- **Backend & Database:** Google Firebase
  - **Firestore:** For the real-time, NoSQL database to store ideas.
  - **Authentication:** For anonymous sign-in to uniquely identify users.

## Setup and Installation

To get your own private, shareable version of this app running, follow these steps.

### 1. Prerequisites

- A modern web browser (like Chrome, Firefox, or Edge).
- A simple text editor (like VS Code, Sublime Text, or even Notepad).
- A Google account to use Firebase.
- A GitHub account.

### 2. Download the App File

- Download or copy the code for the `hangout-spinner.html` file from this project.

### 3. Set Up Your Firebase Project

This app requires a free Firebase project to function as its backend.

1.  **Create a Project:** Go to the [Firebase Console](https://console.firebase.google.com/) and create a new project. Give it any name you like (e.g., "My-Hangout-Scroll").

2.  **Create a Firestore Database:**
    - From the left-hand menu in your Firebase project, go to **Build > Firestore Database**.
    - Click **Create database**.
    - Choose to start in **test mode**. This allows the app to read and write data easily. Click **Next**.
    - Select a location for your database (the default is usually fine) and click **Enable**.

3.  **Enable Anonymous Authentication:**
    - In the left-hand menu, go to **Build > Authentication**.
    - Click **Get started**.
    - Go to the **Sign-in method** tab.
    - Find **Anonymous** in the list of providers, click it, and toggle the **Enable** switch on. Click **Save**.

4.  **Get Your Firebase Keys:**
    - Go back to your project's main page by clicking the gear icon `⚙️` next to **Project Overview** and selecting **Project settings**.
    - In the "Your apps" section, click the web icon (`</>`).
    - Give your web app a nickname (e.g., "Web App") and click **Register app**.
    - Firebase will display a `firebaseConfig` object. It looks like this:
      ```javascript
      const firebaseConfig = {
        apiKey: "AIza...",
        authDomain: "your-project.firebaseapp.com",
        // ...and so on
      };
      ```
    - **Keep this page open!** You will need to copy these keys.

### 4. Configure the HTML File

1.  Open your `hangout-spinner.html` file with your text editor.
2.  Scroll down to the `<script type="module">` section near the bottom.
3.  Find the `const firebaseConfig = { ... };` block.
4.  **Replace the placeholder keys** inside this block with the actual keys from your Firebase project that you just generated.
5.  Save the file.

## Deployment

Once your `hangout-spinner.html` file is configured, you can deploy it to a live URL for free. Here are a couple of popular options.

### Option A: Deploying with GitHub Pages

1.  **Create a GitHub Repository:**
    - Go to [GitHub](https://github.com/) and create a new public repository. Name it something like `hangout-scroll`.

2.  **Upload Your File:**
    - In your new repository, click the **Add file** button and select **Upload files**.
    - Drag and drop your edited `hangout-spinner.html` file into the upload area.
    - It's important to **rename the file to `index.html`** either before you upload it or directly in the GitHub interface. This is the default file GitHub Pages looks for.

3.  **Enable GitHub Pages:**
    - Go to your repository's **Settings** tab.
    - In the left sidebar, click on **Pages**.
    - Under "Branch," select `main` (or `master`) and keep the folder as `/root`. Click **Save**.
    - GitHub will provide you with the live URL for your app (e.g., `https://your-username.github.io/hangout-scroll/`). It may take a minute or two to go live.

### Option B: Deploying with Netlify

1.  **Prepare Your Project:**
    - Create a new folder on your computer.
    - Place your edited `hangout-spinner.html` file inside this folder and rename it to `index.html`.

2.  **Deploy to Netlify:**
    - Go to [Netlify](https://app.netlify.com/drop) and sign up or log in.
    - Simply drag the **folder** containing your `index.html` file onto the deployment area on the Netlify site.
    - Netlify will automatically upload the folder and deploy your site, providing you with a random live URL (e.g., `https://random-name-12345.netlify.app`). You can customize this URL in the site settings.

## Usage

You're all set!

- **To use the app:** Simply share the live URL you got from GitHub Pages or Netlify with your friends.
- As long as everyone visits that URL, you will all be connected to the same shared scroll. Any idea one person adds will appear for everyone else instantly.
      
