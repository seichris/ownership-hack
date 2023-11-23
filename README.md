# Ownership-hack

## Notarize your Twitter account

1. Install Rust with `curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`
2. Get TLSN `git clone https://github.com/tlsnotary/tlsn`
3. Run the notary server
```
cd tlsn/notary-server
cargo run --release
```
4. Download the browser extension from https://github.com/tlsnotary/tlsn-extension/releases/download/0.0.1/tlsn-extension-0.0.1.zip
5. Unzip, and at `chrome://extensions` load unpacked
6. In the extension, click Settings and enter `ws://notary.efprivacyscaling.org:55688` as proxy server
7. Visit https://127.0.0.1:7047 and click `Advanced` and next `Proceed to 127.0.0.1 (unsafe)`. It will say "This site can’t be reached" but it makes the browser successfully accept the certificate.



## Full documentation

For learning how everything works, take this path:

Quickstart: https://docs.tlsnotary.org/developers/quick_start.html
Notarize Twitter without extension: https://github.com/tlsnotary/tlsn/tree/dev/tlsn/examples/twitter
Notarize Twitter with extension: https://github.com/tlsnotary/progcrypto_workshop/blob/main/workshop.md#browser