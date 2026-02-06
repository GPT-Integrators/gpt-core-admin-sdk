# GPT Core Admin SDK

The official TypeScript Admin SDK for GPT Core Platform - tenant management, billing, and platform administration.

## Quick Start

```bash
npm install @gpt-core/admin
```

```typescript
import { GPTCoreAdmin } from '@gpt-core/admin';

const admin = new GPTCoreAdmin({
  apiKey: process.env.GPT_ADMIN_API_KEY,
  baseURL: 'https://api.gptintegrators.com'
});

// List tenants
const tenants = await admin.platform.tenants.list();

console.log(tenants.data);
```

## Documentation

- **[API Reference](https://gpt-integrators.github.io/gpt-core-admin-sdk/docs/admin)** - Interactive API docs with Try It
- **[Quick Start Guide](https://gpt-integrators.github.io/gpt-core-admin-sdk/quickstart)** - Getting started guide

## Tooling

Download API collections for your preferred client:

| Tool | Download |
|------|----------|
| [Postman](https://www.postman.com) | [Download Collection](https://gpt-integrators.github.io/gpt-core-admin-sdk/collections/postman/gpt-core-admin.postman_collection.json) |
| [Bruno](https://www.usebruno.com) | [Browse on GitHub](https://github.com/GPT-Integrators/gpt-core-admin-sdk/tree/main/collections/bruno/admin) |
| [Insomnia](https://insomnia.rest) | [Download Collection](https://gpt-integrators.github.io/gpt-core-admin-sdk/collections/insomnia/gpt-core-admin.insomnia.json) |

## Packages

| Package | Version | Description |
|---------|---------|-------------|
| [@gpt-core/admin](https://www.npmjs.com/package/@gpt-core/admin) | [![npm version](https://badge.fury.io/js/%40gpt-core%2Fadmin.svg)](https://www.npmjs.com/package/@gpt-core/admin) | Admin SDK for platform management |

## Links

- **[Platform Dashboard](https://dashboard.gptintegrators.com)** - Web interface
- **[API Status](https://status.gptintegrators.com)** - Uptime monitoring
- **[Support](mailto:support@gptintegrators.com)** - Get help

## Features

- **Tenant Management** - Create, update, and manage tenants
- **Billing & Credits** - Manage wallets, credits, and transactions
- **User Administration** - User management and access control
- **LLM Analytics** - Usage tracking and cost analysis
- **TypeScript** - Full type definitions included
- **Pagination** - Built-in helpers for paginated responses

## License

Proprietary - All rights reserved. &copy; 2026 GPT Integrators.

## Support

For support, email [support@gptintegrators.com](mailto:support@gptintegrators.com) or contact us through the platform dashboard.
