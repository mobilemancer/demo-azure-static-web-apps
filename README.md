# demo-static-web-apps

Azure Static Web Apps demo.

## Run the project localy

Use the swa cli without installing local using npx.

Start the web application:

```bash
npx @azure/static-web-apps-cli start
```

Starting the web application and the api:

```bash
npx @azure/static-web-apps-cli start --api-location ./api
```

## Routing setup

Prefer routing to a specific endpoint on failed auth?
Add the following section to the config.

```json
"responseOverrides": {
    "401": {
      "redirect": "/login",
      "statusCode": 302
    }
  }
```
