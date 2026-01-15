# Bluey Episode Manager 🐕

A simple web app to browse Bluey episodes, search by name or description, and manage a viewing queue.

## 🌐 Live App

Visit the app at: `https://[your-github-username].github.io/blueyApp/`

*(Replace `[your-github-username]` with your actual GitHub username)*

## Features

- **Browse Episodes**: View all Bluey episodes organized by season
- **Smart Search**: Search episodes by name OR description (e.g., search "xylophone" to find "The Magic Xylophone")
- **Filter by Season**: Quickly filter episodes by season 1, 2, or 3
- **Queue Management**: Click episodes to add them to your watch queue
- **YouTube Player**: Built-in player with auto-play through your queue
- **Persistent Storage**: Your queue and custom episodes are saved locally
- **Add Custom Episodes**: Add your own episode URLs when you find working links

## How to Use

1. **Search for Episodes**: Type in the search box to find episodes by name or what happens in them
2. **Filter by Season**: Use the dropdown to show only episodes from a specific season
3. **Add to Queue**: Click any episode card to add it to your queue (turns green)
4. **Watch**: Click "Play" on any queued episode or "Play All Queued" to start from the beginning
5. **Add Episodes**: Click "Add New Episode" to add YouTube links you find

## Setting Up GitHub Pages

To publish your app online:

1. Go to your repository on GitHub
2. Click **Settings** tab
3. Scroll down to **Pages** section (in the left sidebar)
4. Under **Source**, select **Deploy from a branch**
5. Under **Branch**, select `claude/bluey-episode-web-app-ZvzXU` (or your main branch)
6. Click **Save**
7. Wait a few minutes and your app will be live at the URL shown

## Local Development

To run locally, simply open `index.html` in your web browser. No server required!

## Technologies

- Pure HTML/CSS/JavaScript (no dependencies)
- YouTube IFrame API for video playback
- LocalStorage for data persistence

## Notes

- Most placeholder YouTube URLs in the app are examples and may not work
- When you find working Bluey episode URLs, add them using the "Add New Episode" form
- Your custom episodes and queue are saved in your browser's local storage
- The app works completely offline (except for YouTube video playback)

## Contributing

Found working episode URLs? Have ideas for improvements? Feel free to submit a pull request!

---

Made with 💙 for Bluey fans
