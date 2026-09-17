# Poll Maker Troubleshooting

## MySQL: connection refused

**Symptom:** the server reports `ECONNREFUSED` or cannot connect to MySQL.

**Likely cause:** MySQL is not running, or the host, port, username, or password in your connection settings is wrong.

**Fix:** confirm MySQL is running, run `mysql --version`, then compare your local connection settings with the values used in the server code. Do not share passwords in commits or pull requests.

## Browser: CORS error

**Symptom:** the browser console says a request was blocked by CORS.

**Likely cause:** the frontend and Express server use different addresses or ports and the server has not allowed the browser request.

**Fix:** first confirm the exact frontend and API addresses. Follow the course route setup and use one consistent address; ask the instructor before adding code not yet covered.

## Express: Cannot GET /...

**Symptom:** opening an address shows `Cannot GET /options`.

**Likely cause:** the server is not running, the URL path is wrong, or there is no matching GET route.

**Fix:** start the server, check its terminal output, then compare the browser URL with the route spelling and HTTP method in your Express file.

## npm install fails

**Symptom:** `npm install` prints an error or does not create `node_modules`.

**Likely cause:** Node/npm is not installed correctly, the terminal is in the wrong folder, or the network interrupted the download.

**Fix:** run `node -v` and `npm -v`, use `dir` to confirm `package.json` is in the current folder, then retry the command. Record the first error line when asking for help.

## Port already in use

**Symptom:** Express says the address or port is already in use.

**Likely cause:** another copy of your server is still running.

**Fix:** return to the terminal that started it and press `Ctrl+C`, then start it once. If it persists, choose the course-agreed port and update the frontend URL to match.

## Changes do not appear

**Symptom:** the browser still shows old data or layout.

**Likely cause:** the page was not refreshed, the wrong file is open, or the server was not restarted after a backend change.

**Fix:** save files, refresh the browser, check the terminal, and confirm the URL and project folder.