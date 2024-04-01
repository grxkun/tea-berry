# Tea-Berry: Bridging EVM and Cosmos

![Tea-Berry Logo](https://example.com/tea-berry-logo.png)

**Tea-Berry** is an innovative NPM package that harmoniously connects the **EVM-based blockchain** (think Ethereum) with the **Cosmos chain**. Imagine it as a delightful blend of your favorite tea and the sweet tanginess of berries—bringing together the best of both worlds.

## Features 🌟

- **Interoperability**: Seamlessly transfer assets and data between EVM and Cosmos.
- **Smart Contract Harmony**: Execute EVM smart contracts on the Cosmos chain and vice versa.
- **State Synchronization**: Keep your chai (state) consistent across the two realms.
- **Easy Brewing**: Simple APIs for developers to stir into their projects.

## Installation 🚀

Install the package using NPM:

```bash
npm install tea-berry
```

## Usage 🍵

### Connecting EVM to Cosmos

```javascript
const { TeaBerry } = require('tea-berry');

// Initialize the connector
const connector = new TeaBerry({
  evmNodeUrl: 'https://ethereum-node-url',
  cosmosNodeUrl: 'https://cosmos-node-url',
  privateKey: 'your-private-key',
});

// Listen for EVM transactions
connector.onEvmTransaction((txData) => {
  // Translate EVM transaction data to Cosmos format
  const cosmosTx = translateToCosmosFormat(txData);

  // Sign and broadcast the Cosmos transaction
  connector.sendCosmosTransaction(cosmosTx);
});
```

### Connecting Cosmos to EVM

```javascript
// Listen for Cosmos transactions
connector.onCosmosTransaction((cosmosTx) => {
  // Translate Cosmos transaction data to EVM format
  const evmTx = translateToEvmFormat(cosmosTx);

  // Execute the EVM transaction
  connector.sendEvmTransaction(evmTx);
});
```

## Examples 🌿

Check out the [examples](./examples) directory for aromatic usage samples.

## Contributing 🌱

Contributions are steeped to perfection! Please follow our [contribution guidelines](./CONTRIBUTING.md).

## License 🍓

This project is licensed under the **MIT License**—sip responsibly!

---