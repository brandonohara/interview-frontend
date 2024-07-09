# Interview Requirements

Hello! Thank you for taking a bit of time to show us your technical skills.

-   Download this repository, and install the JS dependencies below.
-   Read through the desired outcomes of this application.
-   Create a simple solution for the outcomes, this should take around 30 minutes to one hour.
-   Build the code, zip this folder, and email the contents to brandon@trak.io

## Project Desired Outcomes

This project should read a list of Trak workspaces from the `websites.txt` file and monitor the health of those applications through it's public health API endpoint.

### On Page Load

1. Display loading state.
2. Read websites from txt file into an array or object.
3. Render websites into example table. (Given in index.html)
4. Use axios on each website's health endpoint.
   a. If website is healthly, it will return a JSON object with the workspace's version, name, and logo. Render these attributes into the table.
   b. Otherwise, display an unhealthy indicator next to the website.
5. Set an interval to check the health of the websites every 5 minutes.
6. Implement logic into the Refresh button to start the health checks manually. Note that this button should be disabled when already running.

### Style Updates

1. On mobile, only display the workspace and health columns.
2. If a workspace is unable to load, use a default placeholder logo but hide the workspace name.

### Health Endpoint

Use axios to make a GET request to each workspace's `/api/v1/workspace` endpoint. An example for staging would be `https://staging.trak.io/api/v1/workspace`

Please note that unhealthy.trak.io should fail as it doesn't exist. dev and staging also have CORS disabled for this example.

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```
