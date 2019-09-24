# My Progress with the tutorial

## Setup

- fork https://github.com/angular/angular-phonecat.git
- git clone --depth=16 https://github.com/EmbraceLife/angular-phonecat.git
- simply run `npm install`, but having too many errors
- keep reading to install properly

**Notice**

The chrome launcher installation caused many error, I removed it from the package.json file and reinstalled the latest version. Meanwhile, I did the same to firefox-launcher although it didn't cause any problem.

```json
"karma-chrome-launcher": "^2.2.0",
"karma-firefox-launcher": "^1.1.0",
```

run `npm install --save-dev karma-chrome-launcher karma-firefox-launcher` and then the latest version I installed are:

```json
"karma-chrome-launcher": "^3.1.0",
"karma-firefox-launcher": "^1.2.0"
```


