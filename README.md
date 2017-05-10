#  [Next.js](https://zeit.co/blog/next2) on Heroku

Deploy [React](https://facebook.github.io/react/)-based universal web apps on [Heroku](https://www.heroku.com/home).

**Demo deployment** from this repo:  
https://nextjs.herokuapp.com

**A custom Node/Express server** is supported. Use it to:

* combine a Node API with a Next/React UI
* implement custom URL routes

▶️ **[Next with custom Express server](https://github.com/mars/heroku-nextjs-custom-server-express)**

## Requires

* Heroku
  * [command-line tools (CLI)](https://devcenter.heroku.com/articles/heroku-command-line)
  * [a free account](https://signup.heroku.com)
* [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* [Node.js](https://nodejs.org)
* [Next.js](https://github.com/zeit/next.js)

## Production deployment

Once you have a [Next app working locally](https://github.com/zeit/next.js#how-to-use), you may deploy it for public access.

🌈 In February 2017, [Next was fixed](https://github.com/zeit/next.js/pull/1164) so that it no longer requires a static build path. As a result, the **[Heroku build adapter](https://github.com/mars/heroku-nextjs-build/blob/master/bin/heroku-nextjs-build) is no longer required**. Next may be deployed to Heroku without any special setup.

✏️ *In the following instructions, replace `$APP_NAME` with your own unique app name.*

1. Ensure the app is a git repo, ignoring local-only directories:

   ```bash
   git init
   (echo node_modules/ && echo .next/) >> .gitignore
   ```
1. Create the Heroku app:

   ```bash
   heroku create $APP_NAME
   ```
1. 🚀 Deploy:

   ```bash
   git add .
   git commit -m 'Next.js app on Heroku'
   git push heroku master
   ```
1. ♻️ Deploy changes: add, commit, & push again.
