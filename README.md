# Getting Started

Welcome to the Apitex Cloud ecosystem. This guide will help you initialize your first neural node and connect to the fabric.

## 1. Get Your API Key
To start using Apitex Cloud, you need a unique Pixel Key.
- Visit the dashboard at [apitex.cloud](https://apitex.cloud)
- Navigate to the **Terminal** section.
- Execute the `INIT_KEY` command to generate your credentials.

## 2. Install the Client
You can interact with our fabric using our lightweight CLI or direct HTTP requests.

```bash
# Using NPM
npm install @apitex/core
```

## 3. Connect to the Fabric
Initialize the connection in your application:

```javascript
import { ApitexFabric } from '@apitex/core';

const fabric = new ApitexFabric({
  apiKey: 'YOUR_PIXEL_KEY',
  region: 'neural-central-1'
});

await fabric.connect();
console.log("NEURAL LINK ESTABLISHED.");
```

## 4. Deploy Your First Service
Once connected, you can deploy services directly into the intelligent routing layer:

```javascript
await fabric.deploy({
  name: 'my-first-node',
  strategy: 'adaptive'
});
```

## Next Steps
- Learn more about our [Intelligent Gateway](../features/api-gateway).
- Explore the [System Architecture](../technical/architecture).
- View the full [API Reference](../api/reference).
