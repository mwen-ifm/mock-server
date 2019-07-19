# Mock server for front end developer

## How to use it

### Things you might need to know

Because this mock service is using https://github.com/namshi/mockserver. If you want to add more endpoint or change the response, read the doucments in the official site.
This mock server only gives to an endpoint that returns 500, and one returns 404.

### Start up mock server

`npx mockserver -p 8080 -m .`

### Test your URL

`curl -i http://127.0.0.1:8080/500`

`curl -i http://127.0.0.1:8080/404`

## Why?

Sometimes you want to simulate some errors happend in the backend, currently, there is no simple way in the frontend dev tools can do that. Launching a fake server that response error you want and redirect the specific requests this mock endpoint can archive the samething.

You can use chrome extension like https://github.com/kylepaulsen/ResourceOverride to redirect a specific url to your local mock server and mimic any response you want.

## CORS

Don't forget to add

```
Access-Control-Allow-Origin: *
Access-Control-Allow-Credentials: true
Access-Control-Allow-Methods: *
Access-Control-Allow-Headers: *
```

in the `mock` file so you won't see any CORS related error in your browser.
