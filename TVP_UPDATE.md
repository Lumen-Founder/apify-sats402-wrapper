# TVP Update: Apify SATS-402 Wrapper

The Apify wrapper shows SATS-402 as a permissionless paid-delivery layer for Actor results.

Public positioning:

> Apify already leads in agentic payments with x402/Skyfire. SATS-402 demonstrates an optional Bitcoin-native paid-delivery path for Actor results using Lightning preimage-locked response delivery.

What it proves:

- Apify remains the upstream Actor platform.
- Real upstream mode uses a normal `APIFY_TOKEN`, with `APIFY_API_TOKEN` accepted as an alias.
- No Apify auth, billing, API token, usage-limit, or rate-limit bypass is attempted.
- SATS-402 encrypts Actor dataset items before delivery.
- Local real-LND regtest creates a real hold invoice and pays a real merchant invoice.
- The bridge observes the Lightning preimage and settles the agent-side hold invoice with the same preimage.
- The agent decrypts locally.
- The receipt says `custody: false` and `credit_extended: false`.

Commands:

```bash
npm run demo:real
npm run apify:demo:fixture
export APIFY_TOKEN=...
npm run apify:demo -- --actor apify/rag-web-browser --query "bitcoin lightning agent payments"
```

Public artifacts:

- Wrapper repo: WRAPPER_REPO_URL_PLACEHOLDER
- Apify issue: APIFY_ISSUE_URL_PLACEHOLDER
- Draft PR: APIFY_PR_URL_PLACEHOLDER
