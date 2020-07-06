# ssg5 Sample Site

Super simple site generator using [ssg5](https://github.com/nalmeida/ssg5) submodule and deploying it on Netlify.

⭐️ See this project live: https://ssg5-test.netlify.app/

## Install

1. Clone this repo and you are good to go!

## Local development

Run the `watch` command to generate the files from `./src` to `./dist` folder and start watching the `./src/*` folder.

```
$ ./watch
```

## Deploy to Netlify

Of course you must have a Netlify account, connect it to your git repository and so on.

### 1. Inside the **Continuous Deployment** of your project, config:

**Build command**: `./generate https://YOUR_FULL_URL.app`

**Deploy directory**: `dist`

### 2. Another required configuration is:

Inside **Build image selection** of your project and select:

**Build image**: `Ubuntu Trusty 14.04`

---

[![Netlify Status](https://api.netlify.com/api/v1/badges/effe723e-bb23-4e2f-baf6-1a615e3771f4/deploy-status)](https://app.netlify.com/sites/ssg5-test/deploys)