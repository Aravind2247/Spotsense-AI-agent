# SpotSense Parking Assistant

A static web demo of the SpotSense idea: live street-parking availability for Riga, with a chat assistant and a trust check for user reports.

**Demo data is simulated.** Street coordinates are approximate, and no real cameras are connected.

## What it does
- **Map:** street segments coloured by estimated free bays.
- **Assistant:** ask about a specific street block, for example "Is there parking space available on Ģertrūdes iela between Krišjāņa Barona iela and Aleksandra Čaka iela?". It also predicts availability at a given hour.
- **Reports:** say "Report free on Terbatas iela between Elizabetes iela and Ģertrūdes iela". The trust engine scores it on GPS proximity, camera agreement, consensus and reporter reputation. Old reports fade out over time.
- **Fusion:** a time-of-day prior, camera counts (where a camera exists) and trust-weighted reports are combined per street segment.

## Run it
Open `index.html` in a browser. No build step or server is needed.

## Publish on GitHub Pages
1. Create a new public repository and upload these files.
2. Go to **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
3. After a minute the demo is live at `https://<your-username>.github.io/<repo-name>/`.

## Privacy
The demo stores no photos, plates or faces. Your reputation score stays in your own browser (localStorage).

## Next steps
Replace the simulated data with the real detection pipeline (OpenCV + YOLO) and a backend API.

## License
MIT
