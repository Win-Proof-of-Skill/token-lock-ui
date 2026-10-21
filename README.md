# Win Proof of Skill Token Lock UI

**Website:** [win-pskill.com](https://win-pskill.com)

Simple UI for the Win Proof of Skill (WIN-PSKILL) TokenLock contract. It uses the Liberdus reference frontend styling.

## Fork Notice

This project is a **fork of the [Liberdus Token Lock UI](https://github.com/Liberdus/token-lock-ui)**. We are grateful to the Liberdus team for the foundation this project builds on.

Win Proof of Skill is an independent project and is not affiliated with or endorsed by the Liberdus team. Original copyright and license notices from upstream are retained.

- Upstream project: [Liberdus/token-lock-ui](https://github.com/Liberdus/token-lock-ui)
- Win Proof of Skill server (also a Liberdus fork): see the main project README

## Quick Start

Use any static server (ES modules require HTTP, not `file://`).

Clone with submodules:

```bash
git clone --recurse-submodules <YOUR-WIN-PSKILL-TOKEN-LOCK-UI-REPO-URL> token-lock-ui
cd token-lock-ui
python3 -m http.server 8080
```

If the repo is already cloned:

```bash
git submodule update --init --recursive
python3 -m http.server 8080
```

Open `http://localhost:8080`.

## Network and Contract

All site, network, and contract values are configured in `js/config.js`.

The app resolves an environment from `SITE_ENVIRONMENTS`, or from the `env` query parameter (`?env=bnbtestnet`, `?env=bnbmainnet`, `?env=amoy`, or `?env=hardhat`).

| Environment | Network | Contract |
| --- | --- | --- |
| `bnbtestnet` | BNB Smart Chain Testnet | Set in `js/config.js` |
| `bnbmainnet` | BNB Smart Chain | Set in `js/config.js` after mainnet deployment |
| `amoy` | Polygon Amoy | Set in `js/config.js` |
| `hardhat` | Local Hardhat | Deterministic address of your local deployment |

> **Note:** The contract addresses shipped with the upstream Liberdus repository belong to Liberdus deployments. Replace them in `js/config.js` with the addresses of your own Win Proof of Skill TokenLock deployments before use.

## ABI

Update `abi.json` if the contract changes.

## Notes

- Requires MetaMask for write actions.
- Lock amounts are in token units; inputs are converted using token decimals.
- `ratePerDay` uses `RATE_SCALE = 1e12`.

## Contributing

Issues and pull requests are welcome. If a fix or feature is relevant to the shared codebase, please consider contributing it upstream to [Liberdus/token-lock-ui](https://github.com/Liberdus/token-lock-ui) as well.

## Links

- Website: [win-pskill.com](https://win-pskill.com)
- Upstream: [github.com/Liberdus/token-lock-ui](https://github.com/Liberdus/token-lock-ui)

## License

This project inherits the license of the upstream Liberdus Token Lock UI repository. See the `LICENSE` file for details.
