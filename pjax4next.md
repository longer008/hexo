# [PJAX](https://github.com/MoOx/pjax) for [NexT](https://github.com/theme-next)

# Installation

## If you want to use the CDN instead of clone this repo, please jump to the Step 3.

## Step 1 → Go to NexT dir

Change dir to **NexT** directory. There must be `layout`, `source`, `languages` and other directories:

```
$ cd themes/next
$ ls
_config.yml  crowdin.yml  docs  gulpfile.js  languages  layout  LICENSE.md  package.json  README.md  scripts  source
```

## Step 2 → Get module

Install module to `source/lib` directory:

```
$ git clone https://github.com/theme-next/theme-next-pjax source/lib/pjax
```

## Step 3 → Set it up

Enable module in **NexT** `_config.yml` file and select your theme:

```
pjax: true
```

**And, if you wants to use the CDN, then need to set:** (you also need to find your corresponding theme css link in [jsdelivr](https://www.jsdelivr.com/package/npm/pjax-js?path=themes))

```
vendors:
  ...
  pjax: //cdn.jsdelivr.net/gh/theme-next/theme-next-pjax@0/pjax.min.js
```

# Update

```
$ cd themes/next/source/lib/pjax
$ git pull
```