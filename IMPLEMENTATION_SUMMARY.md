# Token Distribution Implementation Summary

The fork includes an experimental Foundry script at
[`ethereum/forge-scripts/DistributeTokens.s.sol`](ethereum/forge-scripts/DistributeTokens.s.sol).
It exposes batch and single-recipient methods and blocks broadcasting while its
owner addresses are placeholders. The token contract enforces its own mint
permissions.

The [example configuration](ethereum/config/distribution-config.json) is a
reference for manual configuration. The script uses its Solidity constants and
command-line arguments. The `dryRun` method validates batch structure locally.
Testing on a local chain or testnet is required to verify mint permissions and
transaction behavior.

The GitHub Actions distribution workflow has been retired. Keep signing keys out
of CI. See the [deployment guide](DEPLOYMENT_GUIDE.md) and
[configuration README](ethereum/config/README.md) for local testing.
