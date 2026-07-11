# Heartwood App Store

This is an [Umbrel](https://umbrel.com) community app store containing a single app:

- **Heartwood** — a self-hosted Bitcoin command center featuring a block
  explorer, watch-only wallets, PSBT construction, hardware-wallet signing,
  multisig, and multi-user access with passkeys, all running against your own
  node. Ships as a prebuilt, multi-arch image at
  [`ghcr.io/alexm223/cairn`](https://github.com/AlexM223/cairn).

## Add this store to your Umbrel

1. Open the **App Store** on your Umbrel.
2. Click the three-dots menu → **Community App Stores**.
3. Paste in this URL and submit:

   ```
   https://github.com/AlexM223/heartwood-app-store.git
   ```

4. Install **Heartwood** from the newly added store.

## First run

- Sign in with the username `admin@cairn.local` and the password shown on the
  app's install card in Umbrel.
- These initial credentials are single-use: you'll immediately be prompted to
  set your own email and password, and the bootstrap credentials cannot be
  reused after that.
- Hardware-wallet signing (WebHID/WebSerial) requires a secure browser
  context, so it's served over HTTPS at `https://<your-umbrel-host>:5588`.
  Your browser will warn about the self-signed certificate Heartwood
  generates on first boot — accept it to continue. Everything else works
  over the normal app URL.
- Configure your chain backend (your own Electrum server or Bitcoin Core RPC)
  under **Settings → Chain Backend** after logging in. No external services
  are contacted.

## App details

| | |
|---|---|
| App ID | `heartwood-bitcoin` |
| HTTP URL | `:3217` |
| HTTPS hardware-wallet URL | `:5588` |
| Image | Pinned by digest, multi-arch (`ghcr.io/alexm223/cairn`) |
