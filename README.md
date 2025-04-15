# How-to-Run-an-InitVerse-Node-step-by-step-guide


> **Disclaimer**: I’m a community member sharing an educational tutorial on setting up an InitVerse node. I’m not an official representative of InitVerse. This guide is for informational purposes only and is **not financial advice**. Always do your own research.

---

## ✅ Step 1: Setting Up a VPS

Choose a VPS provider like **Contabo**, **DigitalOcean**, or **AWS**.  
For this guide, a small plan like **Contabo’s CLOUD VPS 2** (or equivalent) works well.  
👉 [Use this Contabo VPS Link](https://www.tkqlhce.com/5k117cy63y5LNMNPTTSSSLNRMOOPST?sid=medium)

- Select **Ubuntu 22.04**

---

## ✅ Step 2: Connect to Your VPS

```bash
ssh root@<IP_OF_YOUR_VPS>
```

---

## ✅ Step 3: Configure Your Node

**Update your system:**

```bash
sudo apt-get update
```

**Install Screen:**

```bash
apt install screen
```

**Download Inichain file:**

```bash
wget https://github.com/Project-InitVerse/ini-miner/releases/download/v1.0.0/iniminer-linux-x64
```

**Give permission to the file:**

```bash
chmod +x iniminer-linux-x64
```

**Create a new screen session:**

```bash
screen -S Inichain
```

### 🧪 Launch the InitVerse miner (testnet)

```bash
./iniminer-linux-x64 --pool stratum+tcp://<YOUR_WALLET_ADDRESS>.Worker001@pool-core-testnet.inichain.com:32672
```

### 🌐 Launch the InitVerse miner (mainnet)

```bash
./iniminer-linux-x64 --pool stratum+tcp://<YOUR_WALLET_ADDRESS>.Worker001@pool-a.yatespool.com:31588
```

**Leave the screen session:**

```bash
CTRL + A + D
```

---

## ✅ Step 4: Check Your Miner Activity

- 🔍 **Testnet Dashboard**: [https://genesis-testnet.yatespool.com/](https://genesis-testnet.yatespool.com/)
- 🌍 **Mainnet Dashboard**: [https://a.yatespool.com/](https://a.yatespool.com/)

> Paste your wallet address to view miner stats.

### 🎁 Rewards

- Rewards are automatically sent to your wallet address.
- You can check them on the explorer:  
  🔗 [https://genesis-testnet.iniscan.com/](https://genesis-testnet.iniscan.com/)

### 🧾 Check Logs

To reattach the screen and see logs:

```bash
screen -r Inichain
```

To exit again:

```bash
CTRL + A + D
```


