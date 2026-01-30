# about xypher tool

## educational purpose only
**notice: this tool is created for educational and research purposes only.** it is designed to demonstrate how session management and automation interact with web apis. 

## how it works
the tool utilizes the facebook business api and graph api to perform actions. here is a breakdown of the core mechanisms:

### 1. session management (cookies)
the tool uses browser-like session cookies to maintain authentication. it retrieves these by simulating a login request to facebook’s authentication endpoints or by accepting manual cookie strings.

### 2. cookie verification
to ensure the automation doesn’t fail, the script regularly tests cookies against `business.facebook.com`. if a cookie is redirected to a login page, it is marked as "dead" and moved to a backup file (`dead_cookies.txt`).

### 3. automation logic
- **sharing**: uses the graph api `me/feed` endpoint to create post links.
- **commenting**: (unavailable) - uses the graph api `{post_id}/comments` endpoint.
- **reacting**: (ongoing maintenance) the auto react feature is currently under repair to ensure compatibility with updated security protocols.
- **concurrency**: employs python's `threading` library to perform actions in parallel, significantly increasing speed while allowing for user-defined delays to mimic human behavior.

### 4. security & ethics
users are responsible for their own actions. using automation tools on social platforms can lead to account restrictions or bans. always respect the terms of service of the platforms you interact with.
