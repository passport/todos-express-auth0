# todos-express-auth0

This app illustrates how to use [Passport](https://www.passportjs.org/) with
[Express](https://expressjs.com/) to sign users in via [Auth0](https://auth0.com/).
Use this example as a starting point for your own web applications.

## Quick Start

To run this app, clone the repository and install dependencies:

```bash
$ git clone https://github.com/passport/todos-express-auth0.git
$ cd todos-express-auth0
$ npm install
```

This app must be configured with an Auth0 domain, as well as a client ID and
secret that has been created for the app.

Once credentials have been obtained, create a `.env` file and add the following
environment variables:

```
AUTH0_DOMAIN=example.us.auth0.com
AUTH0_CLIENT_ID=__INSERT_CLIENT_ID_HERE__
AUTH0_CLIENT_SECRET=__INSERT_CLIENT_SECRET_HERE__
```

Start the server.

```bash
$ npm start
```

Navigate to [`http://localhost:3000`](http://localhost:3000).

## Tutorial

Follow along with the step-by-step [Auth0 Tutorial](https://www.passportjs.org/tutorials/auth0/)
to learn how this app was built.

## Overview

This app illustrates how to build a todo app with sign in functionality using
Express, Passport, Auth0, and the [`passport-openidconnect`](https://www.passportjs.org/packages/passport-openidconnect/)
strategy.

This app is a traditional web application, in which application logic and data
persistence resides on the server.  HTML pages and forms are rendered by the
server and client-side JavaScript is not utilized (or kept to a minimum).

This app is built using the Express web framework.  Data is persisted to a
[SQLite](https://www.sqlite.org/) database.  HTML pages are rendered using [EJS](https://ejs.co/)
templates, and are styled using vanilla CSS.

When a user first arrives at this app, they are prompted to sign in.  To sign
in, the user is redirected to our app's sign in page (which is hosted by Auth0)
using OpenID Connect.  Once authenticated, a login session is established and
maintained between the server and the user's browser with a cookie.

After signing in, the user can view, create, and edit todo items.  Interaction
occurs by clicking links and submitting forms, which trigger HTTP requests.
The browser automatically includes the cookie set during login with each of
these requests.

## License

[The Unlicense](https://opensource.org/licenses/unlicense)

## Credit

Created by [Jared Hanson](https://www.jaredhanson.me/)
