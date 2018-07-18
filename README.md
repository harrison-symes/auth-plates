# A starter webpack project for React, Redux, Express and Knex, Auth

This is a rad base for starting a new full-stack project + Auth, or just as reference for how to do things the Harrison way (which is with absolutely no test folder, I'll leave that one to Alan)

## Init

* Fork this repo to your github
* Rename your repo according to the app you're building

To start a new project:
  * Make a new repo on github
  * `git clone https://github.com/harrison-symes/auth-plates.git <NEW REPO NAME HERE>`
  * `git remote remove origin`
  * `git remote add origin <NEW REPO URL HERE`
  * `git remote -v` to see your remotes
  * `git push origin master` to push the boilerplate code to your new repo

## Setup

Run the following commands in your terminal:

```sh
yarn install
yarn knex migrate:latest
yarn knex seed:run
mv .env_example .env
```

To run in development:
```sh
yarn dev
 - or -
npm run dev

```

To run in production:
```sh
yarn start
  - or -
npm start
```


## Heroku!!!

### Creating your app

Create your app with `heroku create [name]`

You can check that this was successful by running `heroku apps` to view a list of your apps


### Adding postgres

Add postgresql (hobby dev) to your app at `https://dashboard.heroku.com/apps/[APP NAME HERE]/resources`

Check that pg has been added by running `heroku addons` to ensure the postgresql db is on your app


### Deploying!

I have created several npm scripts that will be useful for deploying your app to heroku easily.

To push your local master branch to your heroku app:
```sh
yarn h:deploy
  - or -
npm run h:deploy
```

Run heroku migrations:
```sh
yarn h:migrate
  - or -
npm run h:migrate
```

Run heroku seeds:
```sh
yarn h:seed
  - or -
npm run h:seed
```

If ever you need to rollback, you can also:
```sh
yarn h:rollback
  - or -
npm run h:rollback
```


### Ta-Da!
Your app should be deployed!
