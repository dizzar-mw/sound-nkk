# Sound-Nkk — Local Talent, Global Vibes

A responsive React + Vite starter concept for a Malawi-focused platform where local musicians can showcase music, videos, events and promotions. Theme: black, deep green and aqua.

## Included
- Responsive home page, artist cards, track cards, trending list and community feed
- Search and genre filters
- Demo booking modal (name, phone, date, event details)
- Local media file preview
- Editable community location in demo mode
- Popular comments sorted by comment count
- Artist cards, event panels, recent conversations and promo UI
- GitHub Pages-friendly relative asset/build configuration
- Firebase and Leaflet dependencies included for the next integration step

## Run locally
Install Node.js 20 or newer, then run:

```bash
npm install
npm run dev
```

To build:
```bash
npm run build
```
The generated site is in `dist/`.

## GitHub Pages
1. Create a GitHub repository and upload these files.
2. In the repository, go to **Settings → Pages** and choose **GitHub Actions**.
3. Add a workflow to build with `npm ci` and `npm run build`, then upload/deploy `dist/`.
4. If publishing at `https://USERNAME.github.io/REPOSITORY/`, configure Vite's `base` to `'/REPOSITORY/'` (or keep `./` if your deployment setup supports relative paths).
5. Place image assets inside `public/assets/`.

## Add your artwork
Create `public/assets/` and add files such as:
- `hero-musician.jpg`
- `dizzar.jpg`
- `lina-mizi.jpg`
- `kabwee.jpg`
- `nyasa-vibes.jpg`
- `teejay.jpg`
- `mzee-b.jpg`

The starter gracefully falls back to initials if artist photos are missing. The hero uses a CSS background and looks best with `public/assets/hero-musician.jpg`.

## Important production notes
This is a front-end starter and the booking/profile/comments/uploads/messages are demo interactions stored in browser memory only. They do not yet save to a shared database or send real messages.

Before accepting real customer information:
- Configure Firebase Authentication, Firestore and Firebase Storage.
- Add Firebase security rules and admin-role checks; never rely on hiding admin UI in the browser.
- Store booking requests and comments in Firestore and media in Storage.
- Use authenticated access rules for profile photos, uploads and messages.
- Add moderation, abuse reporting, privacy policy and consent/retention practices.
- For actual music playback, integrate a licensed audio player and ensure artists have rights to uploaded content.
- For real donations or paid promotions, integrate a trusted payment provider and validate payment status server-side.
- Add a Leaflet map and a suitable tile provider; configure attribution and any API keys/terms. The current map is an illustrative demo map, not a live aerial map.

## Firebase next step
Create a Firebase project, enable Authentication (email/password or Google), Firestore and Storage, then add a `src/firebase.js` module with your public web app configuration. Apply least-privilege rules before deployment. Firebase web config is not a substitute for security rules.

## Accessibility
The starter includes responsive layout, button labels for common controls and keyboard focus styles. Continue testing with keyboard navigation and screen readers before launch.
