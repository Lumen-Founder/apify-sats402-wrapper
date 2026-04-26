Unofficial proof: Apify Actor results can be wrapped in SATS-402 Bitcoin-native paid delivery.

Apify already leads in agentic payments with x402/Skyfire. SATS-402 is an optional complementary Lightning preimage-locked delivery path.

No Apify auth, billing, API token, usage-limit, or rate-limit bypass.

The proof uses local real-LND regtest:
- real hold invoice
- real merchant invoice payment
- real Lightning preimage observed
- same preimage unlocks encrypted Actor result locally
- custody: false
- credit_extended: false

Demo:
`npm run apify:demo -- --actor apify/rag-web-browser --query "bitcoin lightning agent payments"`

Standalone repo:
https://github.com/Lumen-Founder/apify-sats402-wrapper
