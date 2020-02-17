# node-expose-sspi

Expose the Microsoft Windows SSPI (SSP Interface) to [Node.js®](https://nodejs.org/).

It has been done in order to do NTLM and Kerberos SSO authentication.
You may participate to complete this project if you need to use SSPI in another use case.

This module works only on Microsoft Windows OS.

## Install

Just do:

```
npm i node-expose-sspi
```

Note: There is a prebuilt binary node addon that will be installed.

## Usage

### SSO Authentication use case

```bat
mkdir myproject
cd myproject
npm init -y
npm i express
npm i node-expose-sspi
```

Make an express web server by doing the `server.js` file:

```js
import express = require("express");
import { sso } from "node-expose-sspi";

// global.debug = true;

const app = express();

app.use(sso.auth());

app.use((req, res, next) => {
  res.json({
    sso: req.sso
  });
});

app.listen(3001, () => console.log("Server started on port 3001"));
```

```
node server.js
```

Open a web browser and go to `http://localhost:3001`

#### Typescript

This module is also integrated with Typescript.

[Typescript example](./doc/typescript.md)

#### NTLM

If you are not on a Microsoft Windows Active Directory Domain, it will use the NLTM authentication protocol.

Note: the NTLM protocol is not very secure.

#### Kerberos

You should see (this Node Expose SSPI Kerberos dedicated documentation)[./doc/Kerberos.md].


## Rebuilding the binary

If the provided Windows binary does not work for your OS,
You can rebuild the Node addon binary:

```
cd .\node_modules\node-expose-sspi
npm run build
```

Note: You may need a proper C++ Windows Toolchain installed.
One way to do it is to install this module:

```
npm install --global windows-build-tools
```

## Test and Example

You can run the test and the example only in development.

Just clone this project.

```
git clone https://github.com/jlguenego/node-expose-sspi.git
cd node-expose-sspi
npm i
npm test
npm run example
```

## Develop

To compile the native node module, you need:
```
npm install --global windows-build-tools
```


## TODO

- Check that there is no memory leak.
- Typing flags

## Author

Jean-Louis GUENEGO <jlguenego@gmail.com> (http://jlg-consulting.com/)
