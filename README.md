# Alice Controller

Web controller for a Hyperledger Aries Alice CloudAgent (aca-py)

## Table of Contents

- [Prerequisites](#prerequisites)
- [Running Locally](#running-locally)
    - [Prerequisites](#prerequisites)
    - [Start the Application](#start-the-application)
- [Notes](#notes)

### Running Locally (Steps to start)
Note: Before carrying out the following process, start up the von-network from Docker on localhost:9000, as the agent requires the von-network, and without starting it, it won't work.
Commands:
cd von-network
./manage build
./manage start --logs
visit: localhost:9000

Step 1: Clone the aries-cloudagent-python project in your system from this link:https://github.com/hyperledger/aries-cloudagent-python

Step 2: Starting the holder agent Open git bash and navigate to the folder where the agent project is cloned.

Step 3: Then write the command ACME Agent: cd /aries-cloudagent-python/demo.

Step 4: Then, to run the agent, write ./run_demo alice, and In case of error, docker rm -f alice. Now we have successfully run the agent.

Step 5: Now we will run the controller project. Clone the controller project in your system from the GitHub link:https://github.com/hyperledger/aries-acapy-controllers.(Prerequisite: Node.js needs to be installed), npm install -g @angular/cli	.

Step 6: Navigate to the folder in another bash tab using the command cd /aries-acapy-controllers/AliceFaberAcmeDemo/controllers/alice-controller.

Step 7: Write npm install OR npm install --force

Step 8: To start the production server write ng serve

Step 9: Start the project on localhost:4200

#### Prerequisites

Alice Controller requires `Node.js 10.x` or higher. Node.js can be downloaded [here](https://nodejs.org/en/download/). Alternatively you can use a Node.js version manager like [`nvm`](https://github.com/nvm-sh/nvm) or [`nvm-windows`](https://github.com/coreybutler/nvm-windows).

Alice controller was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.1.1 and can be run locally with minimal effort using the CLI. The CLI is installed as a global npm package.

For example on Linux:

```
$ npm install -g @angular/cli
```

#### Start the Application

From the alice-controller root directory, simply install application node modules then call `ng serve`

For example on Linux:

```
$ npm install
$ ng serve
```

You may see an output like:

```
chunk {connection-connection-module} connection-connection-module.js, connection-connection-module.js.map (connection-connection-module) 306 kB  [rendered]
chunk {credential-credential-module} credential-credential-module.js, credential-credential-module.js.map (credential-credential-module) 17.7 kB  [rendered]
chunk {main} main.js, main.js.map (main) 60.6 kB [initial] [rendered]
chunk {polyfills} polyfills.js, polyfills.js.map (polyfills) 264 kB [initial] [rendered]
chunk {proof-proof-module} proof-proof-module.js, proof-proof-module.js.map (proof-proof-module) 16.7 kB  [rendered]
chunk {runtime} runtime.js, runtime.js.map (runtime) 9.13 kB [entry] [rendered]
chunk {styles} styles.js, styles.js.map (styles) 842 kB [initial] [rendered]
chunk {vendor} vendor.js, vendor.js.map (vendor) 4.63 MB [initial] [rendered]
Date: 2020-01-05T18:47:21.136Z - Hash: 61c4728366fef065089e - Time: 7894ms
** Angular Live Development Server is listening on localhost:4200, open your browser on http://localhost:4200/ **
ℹ ｢wdm｣: Compiled successfully.
```

You can now open your browser tab to `localhost:4200` to see the application.

### Notes

_Note: Alice Controller has already been configured to connect to it's agent on localhost:8031. If the controller is not connected to it's agent you will see a red status indicator on the top right-hand side of the navbar. If the agent is successfully connected, you will see a green status indicator._

