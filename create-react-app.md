# Create React App

## Setting requests to default to a different path than the root `/` path

You can set a different default path for requests by setting the `PUBLIC_URL` environment variable within your npm build script like so:

```bash
"build-local": "PUBLIC_URL='http://localhost:8080/app' react-scripts build",
"build-beta": "PUBLIC_URL='https://example.com/app' react-scripts build",
```

## Setting environment variables to be used within your app

CRA doesn't like you to just go setting your environment variables all willy nilly and will make you use the `REACT_APP_` prefix when doing so.

So, if you wanted to set a `LOCAL` environment variable in your `build-local` npm script, you'd need to name it `REACT_APP_LOCAL` and also reference it with that name within your app.

For example:

```bash
"build-local": "REACT_APP_LOCAL=true react-scripts build"
```

and then you could access it by using `process.env.REACT_APP_LOCAL` within your React app

