# steps to follow

- `git checkout -f step-1`
- remove node_modules and package-lock.json
- update with `"karma-chrome-launcher": "^3.1.0",` in package.json
- run `npm install`
- `git checkout -b step-1-Static-Template-me`
- `npm start` and click `localhost:8000`
- insert `<p>Total number of phones: 2</p>` into app/index.html
- refresh the webpage
- `git push --set-upstream origin step-1-Static-Template-me`
