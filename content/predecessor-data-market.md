# Predecessor Alpha data market

The data-market source preserves the original eip155:5615610 read/write
service, Union Integration Credit terms and admitted EAVT Datom carrier.
The current node producer selects the successor chain in alpha-chain.mjs.
The original account, resource-contract address, token address and payee
remain explicit deployment inputs to this predecessor market.

Run node src/data-market.mjs with EVM_RPC_URL, EVM_KEYSTORE_PATH,
EVM_KEYSTORE_PASSWORD_PATH, ONCHAIN_RESOURCE_CONTRACT and X402_ASSET.
X402_PAY_TO defaults to the supplied account. The original default tariffs
are 1000 write units and 100 read units, overridden by X402_WRITE_AMOUNT
and X402_READ_AMOUNT. HOST and PORT select the listener.

The generic ERC-5219 client is supplied by Ethereum Engineering. The
payment boundary is supplied by x402 Engineering. The purchase command is
scripts/purchase-data.mjs and consumes the payer's explicit keystore paths.
