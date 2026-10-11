# CANOPY — BTCZ Community GPU Camp

An unofficial Telegram mini-app mining game designed for **$BTCZ (BitcoinZ)**.

This is not another tap-a-coin clone. You run a volunteer GPU camp under BitcoinZ’s **Canopy** era: ASIC-resistant Equihash 144,5 lore, a real **2.5-minute block clock**, and a **T-rail / Z-rail split** that mirrors transparent vs shielded addresses.

In-game balance is **ZH** (Zhash credits). It is a prototype score, not a live on-chain payout. Wire a backend + wallet if you want real BTCZ later.

## Why this is unique

| Usual TG miner | CANOPY |
|---|---|
| Tap coin, wait, claim | Overclock a GPU farm, manage heat |
| One token faucet | Dual rails: T = steady, Z = jackpot + luck |
| Fake 1-second “blocks” | **150-second blocks** (BTCZ block time) |
| Hamster / cat / rocket skin | Canopy, Zhash, Vertex, Z-Text, Zebra |
| Only social tasks | Social tasks **plus** hidden games |

Brand palette from the BTCZ mark: gold `#FFA700`, sand `#F8E464`, teal `#42ABCC`, charcoal `#32343D`.

## Screens

- **Mine** — GPU cards, T/Z slider, overclock, heat bar, block countdown
- **Games** — Nonce Rush, Thermal Vent, Shield Memory
- **Tasks** — Follow X, Subscribe YouTube, Join Telegram, visit getbtcz.com, daily streak
- **Rig** — buy Zhash / Canopy / Zebra / Vertex / Z-Text cards
- **Vault** — dossier, local hall, Genesis Cipher

## Hidden games

1. **Night Shift** — tap the empty top-right of the rig panel **5 times**. 2× hashrate.
2. **Z-Vault** — tap the gold **Z shield logo 7 times**, then slide fully to Z-rail and unseal.
3. **Genesis Cipher** — Vault tab, enter `2017` or `nopremine`.
4. **Quiet miner** — tap the flavour text under the heat bar 9 times.

## Official links used in tasks

- X: https://x.com/BTCZOfficial
- YouTube: BitcoinZ Community search / channel
- Telegram: https://t.me/bitcoinzcommunity
- Site: https://getbtcz.com/

Claiming is honor-system in this frontend. To verify follows you need a bot backend (see below).

## Play locally

Open `index.html` in a mobile browser, or:

```bash
cd btcz-canopy
python3 -m http.server 8080
```

Then open `http://localhost:8080`.

## Deploy as a Telegram Mini App

1. Host the folder on HTTPS (Cloudflare Pages, GitHub Pages, Netlify, any static host).
2. Talk to [@BotFather](https://t.me/BotFather)
   - `/newbot` → name it e.g. `Canopy BTCZ Rig`
   - `/newapp` or `/mybots` → Bot settings → Menu Button / Mini App
   - Set the Mini App URL to your hosted `index.html`
3. Optional: `/setmenubutton` so players launch CANOPY from the bot chat.
4. Pin a start message:

> Under the canopy. Split T and Z. Blocks every 2.5 minutes.  
> No premine. Community GPU camp for $BTCZ.

`telegram-web-app.js` is already loaded. The app expands, uses Telegram theme colors, and keys saves to the Telegram user id when present.

## Wiring real verification + real BTCZ later

Minimum backend:

- Store `telegram_id`, ZH, owned GPUs, task flags
- Task verify:
  - X: user pastes profile or you use an official campaign tool
  - YouTube: subscribe + user returns and taps Claim (or YouTube API if you own the channel)
- Payouts: **do not** invent a BTCZ faucet from nothing. Use a community-controlled wallet / multisig and publish the policy. BTCZ is a real PoW coin; this game should never pretend to mint supply.

## Fair-use note

CANOPY is a fan-made community game themed on public BitcoinZ lore (Canopy, Zhash, Vertex, Z-Text, fair launch 2017). It is not the official BitcoinZ team product unless they adopt it.
