# News-Article-RSS
News Article RSS
# RSS News Slideshow

A simple, animated slideshow that pulls headlines and images from an RSS feed, then displays them in a full-screen rotating presentation. Perfect for news displays, digital signage, or any scenario where you want a self-updating news feed.

## Features

- **Auto-updating**: Pulls fresh RSS items every couple of minutes.  
- **Slide rotation**: Cycles through headlines and images every few seconds.  
- **Full-screen experience**: Utilizes CSS animations for subtle fade and scale effects.  
- **Minimal dependencies**: Just HTML, CSS, and vanilla JavaScript—no frameworks needed.

## Getting Started

1. **Clone or Download** this repository.
2. Locate the file `index.html`.
3. Open `index.html` in your browser (double-click it or “Open With…”).  
   - If you see a blank screen or fetch errors, you might need to host the file (see below).

### Hosting on GitHub Pages

1. Go to your repo’s **Settings** → **Pages**.  
2. Under “Build and deployment,” select **“Deploy from a branch.”**  
3. Choose your branch (likely `main`) and the root folder (`/`).  
4. Click **Save**.  
5. After a short build process, you’ll get a URL like:  

https://.github.io//

6. Open that URL to see your slideshow live!

## Configuration

Inside `index.html`, look for the `<script>` section:

```js
const RSS_URL = "https://rss.nytimes.com/services/xml/rss/nyt/US.xml";
const SLIDE_DURATION = 15000;       // 15 seconds
const FEED_REFRESH_INTERVAL = 120000; // 2 minutes
const TRANSITION_DURATION = 500;    // 0.5 seconds

	•	RSS_URL: Change this to any RSS feed link you’d like.
	•	SLIDE_DURATION: How long (in ms) to show each slide.
	•	FEED_REFRESH_INTERVAL: How often (in ms) to re-fetch the RSS feed.
	•	TRANSITION_DURATION: Milliseconds for fade/scale transitions between slides.

How It Works
	1.	On load, the script fetches the RSS feed using fetch().
	2.	It parses the XML to extract <title>, <description>, and <media:content> (if available).
	3.	Renders the first item as a full-screen “slide.”
	4.	A timer rotates to the next slide every SLIDE_DURATION ms, adding a fade/scale effect.
	5.	Every FEED_REFRESH_INTERVAL ms, it re-fetches the feed so new articles appear automatically.

Common Issues
	•	CORS Errors: If the browser blocks the RSS feed, you may need to host this file (rather than open locally) or use a proxy like AllOrigins.
	•	Blank Screen: Check your browser’s developer Console (right-click → “Inspect” → “Console”) for errors. If it’s a fetch or parse error, it’ll show there.

Created By

This project was created by Socrates Lozano.

License

© 2024 Socrates Lozano. All rights reserved.

You are free to use, modify, and distribute this code for personal or commercial projects.

---

### Final Steps

- **Commit** this file to your repository (or upload via GitHub’s web interface).  
- GitHub will automatically display `README.md` at the bottom of the repo’s home page. 
- With that, you’re done! Your project now has clear instructions and info for anyone who visits. 

Enjoy your newly documented RSS Slideshow!
