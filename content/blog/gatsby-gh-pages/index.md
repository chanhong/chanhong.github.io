---
title: Gatsby Blog with gh-pages
date: "2022-03-24T15:48:32.169Z"
description: Steps to create Gatsby site, gh-pages related config then deploy to your GitHub repo.
---

## How to build a Gatsby site on your local hard drive? 

[Gatsby @GitHub](https://github.com/gatsbyjs/gatsby)

## How to add your Gatsby site to your GitHub Repo?

. [Create a new repo](https://docs.github.com/en/get-started/quickstart/create-a-repo)
. Add your new repo to your Gatsby site on your local hard drive using Git-cli
  - git init
  - git branch -M main
  - git remote add origin https://github.com/{yourgithubuser}/{yourrepo}.git
  - git push -u origin main

## How to add your Gatsby site to your GitHub gh-pages branch?

Steps are below:

### How to add gh-pages branch to your GitHub Repo?

  - git branch -M gh-pages
  - git push -u origin gh-pages
  - git branch -M main

### How to add gh-pages related config to package.json?

. Add gh-pages homepage property to package.json:
  - {
    "name": "my-app",
    "version": "0.1.0",
    "homepage": https://{username}.github.io/{repo-name},
. Add gh-pages deployment scripts to package.json:
  - "scripts": {
     "predeploy": "npm run build",
     "deploy": "gh-pages -d build",

### How to deploy your Gatsby site to gh-pages branch of your GitHub repo?

. Deploy your Gatsby site to GitHub repo in gh-pages branch
  - npm run deploy

### How to enable gh-pages branch to show your Gatsby site?

. Set your pages to gh-pages: https://github.com/{yourgithubuser}/{yourrepo}/settings/pages
. Wait until the "Action" is done then you can see your published site at: https://{yourgithubuser}.github.io/{yourrepo}/

All done!