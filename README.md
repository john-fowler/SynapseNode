# SynapseFI-Node-v2
SynapseFI Node.js API Client Library Version 2

## Code Examples
Please refer to [samples.md](samples.md) and our [API documentation](https://docs.synapsefi.com) for examples.

## Setup
Run the following command from the root package directory
```
npm install
```

## Initialization
Require and configure dotenv:
```
require('dotenv').config()
```
Create a .env file at the root directory and add the following variables to it:
```
CLIENT_ID=<YOUR_CLIENT_ID>
CLIENT_SECRET=<YOUR_CLIENT_SECRET>
FINGERPRINT=<YOUR_FINGERPRINT>
```
Initialize new Client:
```
const Client = require('./src/lib/Client');

const client = new Client({
  client_id: process.env.CLIENT_ID,
  client_secret: process.env.CLIENT_SECRET,
  fingerprint: process.env.FINGERPRINT,
  ip_address: '<ip_address>',
  // isProduction boolean determines if production (true) or sandbox (false) endpoint is used
  isProduction: false
});
```

## Testing
Run the following command from the root package directory after the .env file is set up:
```
npm test
```

## License
[MIT License](LICENSE)