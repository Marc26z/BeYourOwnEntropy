# BeYourOwnEntropy

A single-file, offline BIP39 seed entropy lab for **testnet practice only**. It is meant for educational purposes: testnet bitcoin has no value, and this tool is for practice, not for securing real bitcoin.

Open `index.html` directly in a browser, or use the GitHub Pages URL. There is no build step, no server, no dependencies, and no network traffic.

## Features

- D6 dice rolls (100+), using Ian Coleman's exact dice-to-binary mapping; produces standard 12- or 24-word BIP39 phrases
- Coin flips (256+), Heads = 1 / Tails = 0; raw 1/0 input supported
- 23 words drawn from a hat, with the final 3 entropy bits selectable and the BIP39 checksum computed locally
- BIP39 checksum calculated with an embedded SHA-256 and the full 2048-word English list
- Reproducible in Ian Coleman's BIP39 tool with **Dice [1-6]** or **Binary [0-1]** and **Use Raw Entropy (3 words per 32 bits)** — not "24 Words"
- Strict offline CSP, no tracking, no storage, hide-values toggle, clear-all, and print stylesheet

## Companion tool

For testnet practice, once seeds are generated, use [DontTrustVerifyAddresses](https://marc26z.github.io/DontTrustVerifyAddresses/) with its **Network** selector set to **Testnet** to derive printable multisig or single-sig addresses from tpubs. Both pages are offline single-file apps; download them onto the same offline machine before use.

## Security warning

**Educational purposes only — testnet practice.** Testnet bitcoin has no value; this tool is for practice. Keys for spending real bitcoin should never be entered on an online device — never type, paste, or upload real keys or a real recovery phrase here or into any online tool.

**Never use this on an internet-connected computer.** Run it on a genuinely offline machine (for example, TAILS with networking disabled). Use real physical entropy — dice, coins, or paper slips — not an operating system random generator. Each multisig cosigner must generate their own seed independently. See https://airgapcomputer.com/ for operational-security risks.

This tool generates a BIP39 recovery phrase (seed), from which keys are later derived by your wallet/coordinator. It does not create private keys or addresses itself.

## Source

The original single file is preserved as `BeYourOwnEntropy.html`; `index.html` is the identical copy served by GitHub Pages.
