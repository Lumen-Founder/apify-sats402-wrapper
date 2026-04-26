# Summary

Adds a small optional SATS-402 wrapper example/docs pointer for Bitcoin-native paid delivery of Apify Actor results.

This is unofficial and optional. It can be moved, edited, reduced, or closed by maintainers.

Apify already leads in agentic payments with x402/Skyfire. SATS-402 demonstrates a complementary Bitcoin-native paid-delivery path using Lightning preimage-locked response delivery.

Standalone proof repo:

WRAPPER_REPO_URL_PLACEHOLDER

Related issue:

APIFY_ISSUE_URL_PLACEHOLDER

## Notes

- Does not bypass Apify auth.
- Does not bypass Apify billing.
- Does not bypass Apify API tokens.
- Does not bypass Apify usage limits or rate limits.
- Real upstream mode uses a normal `APIFY_TOKEN`.
- Fixture mode supports local verification without an Apify token.
- The proof path uses local real-LND regtest for hold-invoice/payment/preimage settlement.

Demo command:

```bash
npm run apify:demo -- --actor apify/rag-web-browser --query "bitcoin lightning agent payments"
```
