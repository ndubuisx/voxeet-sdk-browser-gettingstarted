# Dolby.io Video Conference Application with Media Devices Controls

## Getting Started

Here is how to set up and run this project locally.

### Prerequisites
* Sign up for a free Dolby.io account [here](https://dashboard.dolby.io/).
* Create a new application and save the Communications API key and secret.

### Installation and Usage
1. Clone this repo and change directory.
    ```sh
    $ git clone https://github.com/ndubuisx/voxeet-sdk-browser-gettingstarted

    $ cd voxeet-sdk-browser-gettingstarted
    ```
    
2. Replace this line in [client.js](./src/scripts/client.js) with your Dolby.io Communications API key and secret.
    ```js
    VoxeetSDK.initialize('customerKey', 'customerSecret');
    ```
    
3. Start a simple http server to access the conference web application
    ```sh
    $ cd src && npx http-server -a localhost -p 8000 -c-1 -o ./

4. Open the application in your web browser at [localhost:8000](http://localhost:8000).


### Why Start a HTTP Server?
Chrome has [deprecated](https://www.chromium.org/Home/chromium-security/deprecating-powerful-features-on-insecure-origins) support for accessing media devices through insecure origins (`http://`) and visiting a local web page through it's HTML file is not recognized as a secure origin (`https://`). However, you can test the Communications API's media devices feature through your machine's localhost since it is treated as a secure origin on Chrome and other Chromium browsers.

Safari on macOS (as of [v15.0](https://developer.apple.com/documentation/safari-release-notes/safari-15-release-notes)) still supports accessing media devices through insecure origins, so you can open the [index.html](./src/index.html) file on there without starting a HTTP server for testing purposes.


