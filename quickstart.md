# Quick Start Guide

Get up and running with the GPT Core Admin SDK in minutes.

## Installation

```bash
npm install @gpt-core/admin
```

## Configuration

Create a admin instance with your API key:

```typescript
import { GPTCoreAdmin } from '@gpt-core/admin';

const admin = new GPTCoreAdmin({
  apiKey: process.env.GPT_ADMIN_API_KEY,
  baseURL: 'https://api.gptintegrators.com'
});
```

### API Key

Get your API key from the [Platform Dashboard](https://dashboard.gptintegrators.com).

### Environment Variables

```bash
# .env
GPT_ADMIN_API_KEY=sk_live_your_key_here
GPT_BASE_URL=https://api.gptintegrators.com
```

## Basic Usage

### List Tenants

```typescript
const tenants = await admin.platform.tenants.list();
console.log(tenants.data);
```

### Manage Credits

```typescript
// Add credits to a tenant
await admin.billing.credits.create({
  tenantId: 'tenant_123',
  amount: 1000,
  reason: 'Monthly allocation'
});
```

### User Management

```typescript
// List users for a tenant
const users = await admin.identity.users.list({
  tenantId: 'tenant_123'
});

console.log(users.data);
```

## Error Handling

```typescript
import { GPTCoreAdmin, ApiError } from '@gpt-core/admin';

try {
  const result = await admin.platform.tenants.list();
} catch (error) {
  if (error instanceof ApiError) {
    console.error('API Error:', error.status, error.message);
    if (error.status === 401) {
      console.error('Invalid API key');
    } else if (error.status === 429) {
      console.error('Rate limit exceeded');
    }
  }
}
```

## Next Steps

- [Full API Documentation](https://gpt-integrators.github.io/gpt-core-admin-sdk/docs/admin)
- [API Collections](https://gpt-integrators.github.io/gpt-core-admin-sdk/collections) for Postman/Bruno/Insomnia

## Need Help?

- Email: [support@gptintegrators.com](mailto:support@gptintegrators.com)
- [API Status](https://status.gptintegrators.com)
