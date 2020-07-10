# ssg5 Sample Site

Super simple site generator using [ssg5](https://github.com/nalmeida/ssg5) submodule and deploying it on Netlify.

⭐️ See this project live: https://ssg5-test.netlify.app/

## Tested on

* MacOS `10.13.6`
* GNU bash, version `3.2.57(1)-release (x86_64-apple-darwin17)`

## Install

1. Clone this repo **including the submodules** and you are good to go!

```
$ git clone --recurse-submodules https://github.com/nalmeida/ssg5-test.git YOUR_FOLDER
```

## Local development

### 1. Basic Configuration

Set the variables inside the `config.txt` file:

* `SRC` (default `./src`): Your source files.
* `DST` (default `./dist`): The distribution files output.
* `SITE_NAME` (default `"SSG5 Test Website"`): Your website name. Always set it inside double quotes `"`.

### 2. Generate

In order to generate the project locally, run the `generate` command passing the local web server (`base_url`) as a paramenter. It is only used on the `sitemap.xml` generation. If empty, it will use `/` as default.

```
$ ./generate
```

### 3. Replace `base_url`

It is possible do "inject" the `base_url` into all the files inside the `./dist` folder recursively.  If empty, it will use `/` as default.

```
$ ./replace_base_url
```

### 4. Watch the ./src folder

Run the `watch` command to `generate` and `replace_base_url` the files from `./src` to `./dist` folder and start watching the `./src/*` folder.

```
$ ./watch
```

### 5. Serve a local webserver

There is a `./server` shell command to serve the files inside the `./dist` folder. It is a simple wrapper of the `python -m http.server` (tested using the `Python 3.7.3`).

```
$ ./server
```

## Deploy to Netlify

Of course you must have a Netlify account, connect it to your git repository and so on.

### 1. Inside the **Continuous Deployment** of your project, config:

* **Build command**: `./generate https://YOUR_FULL_URL && ./replace_base_url https://YOUR_FULL_URL`
* **Deploy directory**: `dist`

### 2. Another required configuration is:

Inside **Build image selection** of your project and select:

* **Build image**: `Ubuntu Trusty 14.04`

---

[![Netlify Status](https://api.netlify.com/api/v1/badges/effe723e-bb23-4e2f-baf6-1a615e3771f4/deploy-status)](https://app.netlify.com/sites/ssg5-test/deploys)