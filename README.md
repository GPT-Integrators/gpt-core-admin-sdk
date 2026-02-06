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
  baseURL: 'https://api.gptplatform.com'
});

// List tenants
const tenants = await admin.platform.tenants.list();

console.log(tenants.data);
```

## Documentation

- **[API Reference](/docs/admin)** - Interactive API docs with Try It
- **[Quick Start Guide](/quickstart)** - Getting started guide

## Tooling

Download API collections for your preferred client:

| Tool | Download |
|------|----------|
| [Postman](https://www.postman.com) | [Download Collection](/collections/postman/gpt-core-admin.postman_collection.json) |
| [Bruno](https://www.usebruno.com) | [Browse Folder](/collections/bruno/admin/) - Clone the Bruno folder |
| [Insomnia](https://insomnia.rest) | [Download Collection](/collections/insomnia/gpt-core-admin.insomnia.json) |

## Packages

| Package | Version | Description |
|---------|---------|-------------|
| [@gpt-core/admin](https://www.npmjs.com/package/@gpt-core/admin) | [![npm version](https://badge.fury.io/js/%40gpt-core%2Fadmin.svg)](https://www.npmjs.com/package/@gpt-core/admin) | Admin SDK for platform management |

## Links

- **[Platform Dashboard](https://dashboard.gptplatform.com)** - Web interface
- **[API Status](https://status.gptplatform.com)** - Uptime monitoring
- **[Support](mailto:support@gptplatform.com)** - Get help

## Features

- **Tenant Management** - Create, update, and manage tenants
- **Billing & Credits** - Manage wallets, credits, and transactions
- **User Administration** - User management and access control
- **LLM Analytics** - Usage tracking and cost analysis
- **TypeScript** - Full type definitions included
- **Pagination** - Built-in helpers for paginated responses

## License

Proprietary - All rights reserved. &copy; 2025 GPT Integrators.

## Support

For support, email [support@gptplatform.com](mailto:support@gptplatform.com) or contact us through the platform dashboard.
