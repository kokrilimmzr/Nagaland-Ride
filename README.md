# Nagaland Ride — mobile demo

A small mobile-first progressive web app prototype for passenger and driver flows. It is designed to be easy to test on Android.

## Included
- Passenger and driver demo views
- Dimapur and Kohima city selection
- Pickup/destination choices and illustrative fare estimate
- Demo ride requests, driver acceptance, and cancellation
- Local browser storage
- PWA manifest, icon, and service worker for installation/offline shell

## Important limitations
This is a front-end prototype only. It has **no backend**, no real user accounts, no shared passenger/driver data across devices, no live map/GPS, no real dispatch, no payments, and no identity or vehicle verification. Demo ride requests are saved in the same browser/device only. Fares and distances are fictional estimates and must not be used as commercial quotes.

## Fastest way to test on Android
1. Extract the ZIP.
2. Open `index.html` in a browser to test basic UI. Some browser features, especially PWA installation/offline caching, require hosting over HTTPS.
3. For an installable test version, publish these files to a static HTTPS host (for example GitHub Pages).
4. On your Android phone, open the published HTTPS URL in Chrome.
5. Open Chrome's menu (⋮) and choose **Install app** or **Add to Home screen** if offered.

## Deploy with GitHub Pages
1. Sign in to GitHub and create a new repository, e.g. `nagaland-ride-demo`.
2. Upload `index.html`, `manifest.webmanifest`, `sw.js`, `icon.svg`, and this README to the repository root.
3. Open **Settings → Pages**.
4. Under build/deployment, choose deploy from the `main` branch and `/ (root)`, then save.
5. Wait for the Pages URL to appear. Open that HTTPS URL on Android Chrome.
6. Test passenger request, switch to Driver, set the same city, go online, and accept the request.

## Suggested next development stage
Replace localStorage with a secure backend before testing across devices. A practical next stack is:
- Frontend: React or plain HTML/CSS/JS for MVP
- Authentication: managed auth provider
- Database/API: Supabase or Firebase with strict access rules/server-side authorization
- Maps and routing: licensed mapping API with real routing and location permissions
- Admin: approval of drivers, document review, incident and trip audit tools

Do not collect real passenger data or use this prototype to arrange paid public rides.
