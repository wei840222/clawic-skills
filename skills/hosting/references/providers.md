# Provider and Platform Considerations

## Platform Hosting

Compare current plan limits at the provider’s official pricing and limits page before recommending a tier. Free plans can restrict bandwidth, build minutes, function invocations, commercial use, or team access. Treat provider-specific limits as mutable facts rather than fixed numbers.

- Static assets remain more portable than provider-specific functions, databases, and build integrations.
- Use preview deployments for branch review, then verify the production environment separately.
- Serverless functions can have cold-start latency; assess this against the workload’s latency needs.

## Data Services

Most application platforms require a separate database service. Select its region alongside the application region. For serverless workloads, use the database provider’s documented pooling or serverless connection option when direct connections can exhaust the database limit.

## Research Sources

- Vercel, “Limits” — https://vercel.com/docs/limits
- Netlify, “Pricing and plans” — https://www.netlify.com/pricing/
- Railway, “Pricing” — https://railway.com/pricing
- Cloudflare, “Pages pricing” — https://www.cloudflare.com/developer-platform/products/pages/
