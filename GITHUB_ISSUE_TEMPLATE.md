# Permissionless SATS-402 wrapper for Apify Actor results

This is an unofficial and permissionless SATS-402 wrapper proof for Apify Actor results.

Apify already leads in agentic payments with x402/Skyfire. SATS-402 demonstrates an optional Bitcoin-native paid-delivery path for Actor results using Lightning preimage-locked response delivery.

It does not bypass Apify auth, Apify billing, Apify API tokens, Apify usage limits, or Apify rate limits. In real upstream mode it uses a normal Apify API token through `APIFY_TOKEN`, or `APIFY_API_TOKEN` as an alias. It also supports fixture mode for local verification without an Apify token.

Demo commands:

```bash
npm run apify:demo:fixture
export APIFY_TOKEN=...
npm run apify:demo -- --actor apify/rag-web-browser --query "bitcoin lightning agent payments"
```

The proof demonstrates Bitcoin-native paid delivery for Apify Actor results:

- Agent requests an Apify Actor result.
- Apify executes an Actor and returns dataset items.
- SATS-402 encrypts the Actor result before delivery.
- The agent pays through a local real-LND regtest bridge.
- The bridge observes a real Lightning preimage.
- The same preimage unlocks the Apify dataset locally.
- A receipt is issued with `custody: false` and `credit_extended: false`.

The core proof uses:

- real local bitcoind
- Agent/Gateway/Merchant LND nodes
- a real hold invoice
- a real merchant payment
- same-hash preimage settlement
- local response decryption

Standalone wrapper repo:

https://github.com/Lumen-Founder/apify-sats402-wrapper

Would Apify maintainers be open to an optional docs/example path for this Bitcoin-native paid-delivery proof? This is not a forced merge request and can be moved, renamed, shortened, or closed if it does not fit the project direction.
