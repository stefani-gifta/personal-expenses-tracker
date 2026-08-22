For a **local frontend test before deploying**, do this:

1. Keep your Apps Script backend deployed. Local testing still uses that backend.

2. Temporarily set the real Apps Script URL in `index.html`:

```javascript
const webAppUrl = "https://script.google.com/macros/s/YOUR_DEPLOYMENT_ID/exec";
```

3. Start the local server from the project folder:

```bash
python3 -m http.server 4173
```

4. Open the address (localhost)

5. When testing is complete, stop the server with:

```text
Ctrl+C
```

6. Before committing and deploying, restore the placeholder:

```javascript
const webAppUrl = "WEB_APP_URL";
```