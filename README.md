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
