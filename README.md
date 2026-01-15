# Bluey Episode Manager 🐕

A simple web app to browse Bluey episodes, search by name or description, and create YouTube playlists directly in your account!

## 🌐 Live App

Visit the app at: `https://[your-github-username].github.io/blueyApp/`

*(Replace `[your-github-username]` with your actual GitHub username)*

## ✨ Features

### Core Features
- **Browse Episodes**: View all Bluey episodes organized by season
- **Smart Search**: Search episodes by name OR description (e.g., search "xylophone" to find "The Magic Xylophone")
- **Filter by Season**: Quickly filter episodes by season 1, 2, or 3
- **Queue Management**: Click episodes to add them to your watch queue
- **YouTube Player**: Built-in player with auto-play through your queue
- **Persistent Storage**: Your queue and custom episodes are saved locally
- **Add Custom Episodes**: Add your own episode URLs when you find working links

### 🎬 NEW: YouTube Integration
- **Create Real Playlists**: Connect your YouTube account and create actual playlists from your queue
- **Watch in YouTube**: Opens your newly created playlist directly in YouTube (perfect for Chrome!)
- **OAuth Authentication**: Secure Google sign-in
- **Private Playlists**: Playlists are created as private by default

## 🚀 How to Use

### Basic Usage
1. **Search for Episodes**: Type in the search box to find episodes by name or what happens in them
2. **Filter by Season**: Use the dropdown to show only episodes from a specific season
3. **Add to Queue**: Click any episode card to add it to your queue (turns green)
4. **Watch in App**: Click "Play" on any queued episode or "Play All Queued" to start from the beginning
5. **Add Episodes**: Click "Add New Episode" to add YouTube links you find

### 🎬 Creating YouTube Playlists
1. **Connect Account**: Click "Connect YouTube Account" and sign in with Google
2. **Build Your Queue**: Add episodes you want to watch
3. **Create Playlist**: Click "Create YouTube Playlist from Queue"
4. **Watch in YouTube**: The playlist opens automatically in a new tab - perfect for watching in Chrome!

## ⚙️ Setup Instructions

### Setting Up YouTube API (Optional - for Playlist Creation)

To enable the "Create YouTube Playlist" feature, you'll need to set up Google Cloud credentials:

1. **Create a Google Cloud Project**
   - Go to [Google Cloud Console](https://console.cloud.google.com/)
   - Create a new project or select an existing one

2. **Enable YouTube Data API v3**
   - In your project, go to "APIs & Services" > "Library"
   - Search for "YouTube Data API v3"
   - Click "Enable"

3. **Create OAuth 2.0 Credentials**
   - Go to "APIs & Services" > "Credentials"
   - Click "Create Credentials" > "OAuth client ID"
   - Choose "Web application"
   - Add authorized JavaScript origins:
     - `http://localhost` (for local testing)
     - `https://[your-username].github.io` (for production)
   - Add authorized redirect URIs:
     - `http://localhost`
     - `https://[your-username].github.io/blueyApp/`
   - Copy your **Client ID**

4. **Create API Key**
   - Click "Create Credentials" > "API key"
   - Copy your **API Key**
   - (Optional) Restrict the key to YouTube Data API v3

5. **Update index.html**
   - Open `index.html`
   - Find lines 333-334:
     ```javascript
     const CLIENT_ID = 'YOUR_CLIENT_ID.apps.googleusercontent.com';
     const API_KEY = 'YOUR_API_KEY';
     ```
   - Replace with your actual credentials

**Note**: The app works fine without YouTube API credentials - you just won't be able to create playlists. All other features work normally!

### Deploying to GitHub Pages

This project uses **GitHub Actions** for automatic deployment. Every time you push to your branch, it automatically deploys!

**Setup Steps:**

1. Go to your repository on GitHub
2. Click **Settings** tab
3. Go to **Pages** section (in the left sidebar)
4. Under **Source**, select **GitHub Actions**
5. The workflow is already configured in `.github/workflows/deploy.yml`
6. Push any changes to trigger deployment
7. Your app will be live at: `https://[your-username].github.io/blueyApp/`

**Manual Deployment (Alternative):**
- The GitHub Action runs automatically on push to `main` or your feature branch
- You can also trigger it manually from the "Actions" tab > "Deploy to GitHub Pages" > "Run workflow"

## Local Development

To run locally, simply open `index.html` in your web browser. No server required!

## 🛠 Technologies

- **Frontend**: Pure HTML/CSS/JavaScript (no build step needed!)
- **YouTube IFrame API**: For embedded video playback
- **YouTube Data API v3**: For playlist creation
- **Google Identity Services**: OAuth 2.0 authentication
- **LocalStorage**: Persistent data storage
- **GitHub Actions**: Automated deployment

## 📝 Notes

- Most placeholder YouTube URLs in the app are examples and may not work
- When you find working Bluey episode URLs, add them using the "Add New Episode" form
- Your custom episodes and queue are saved in your browser's local storage
- The app works completely offline (except for YouTube video playback)
- YouTube API integration is optional - all core features work without it

## 🔧 Troubleshooting

### YouTube Playlist Creation Issues

**"Error creating playlist"**
- Make sure you've set up your API credentials correctly
- Check that YouTube Data API v3 is enabled in Google Cloud Console
- Verify your authorized JavaScript origins include your site's URL

**"Please connect to YouTube first"**
- Click the "Connect YouTube Account" button
- Allow the required permissions in the popup

**Videos not added to playlist**
- Some video URLs may be invalid or demo URLs
- Only valid YouTube video IDs will be added to playlists
- Check the browser console for specific error messages

### GitHub Pages Deployment Issues

**Site not updating**
- Check the "Actions" tab to see if the workflow ran successfully
- Make sure GitHub Pages is set to deploy from "GitHub Actions" (not a branch)
- Wait a few minutes - GitHub Pages can take time to update
- Clear your browser cache

## Contributing

Found working episode URLs? Have ideas for improvements? Feel free to submit a pull request!

---

Made with 💙 for Bluey fans
