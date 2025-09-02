# Irys Storage CLI Node Run Full Guide (PC Only)

### Offical Docs by Irys - https://docs.irys.xyz/build/d/storage-cli/installation

----

## 🧰 Prerequisites
	
### Nothing

----

1️⃣ Dependencies for WINDOWS & LINUX & VPS
```
sudo apt-get update && sudo apt-get upgrade -y
```
```
sudo apt install curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev  -y
```
```
sudo apt install -y libssl-dev ca-certificates
```

2️⃣ Install Node JS & NPM
```
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash - && sudo apt install -y nodejs
```
```
node -v
npm -v
```

3️⃣ Install IRYS CLI
```
sudo npm i -g @irys/cli
```

4️⃣ Verify The Installation
```
irys
```

5️⃣ Fund Your wallet [Testnet/Devnet]

>Now, You have to deposit testnet tokens (any chain) 

```
irys fund 1000000 \
  -n devnet \
  -t ethereum \
  -w Private_Key \
  --provider-url RPC_URL
```

* Take Faucet: [Ethereum_Sepolia_Faucet](https://sepolia-faucet.pk910.de/) :: If u have to do in another chain then take faucet of that network:
* The fund amount is in `wei`
* Replace `Private_key` with your actual one (Without 0x)
* Replace `RPC_URL` with your selected network [Link](https://sepolia.drpc.org)

<img width="1493" height="316" alt="481816277-a5b83397-9be0-4204-89d9-b1c1fff419a8" src="https://github.com/user-attachments/assets/023bacd8-466b-46b5-be7f-b39b471fce12" />


6️⃣ Check Balance 

```
irys balance WALLET_ADDRESS \
  -t ethereum \
  -n devnet \
  --provider-url RPC_URL
```

* Replace `WALLET_ADDRESS` with ur actual one & `RPC_URL` too

7️⃣ Upload a File

```
irys upload FILE_PATH \
  -n devnet \
  -t ethereum \
  -w PRIVATE_KEY \
  --tags FILE_PATH FILE_FORMAT \
  --provider-url RPC_URL
```

* Replace FILE_PATH with their actual path & `FILE_FORMAT` (JPG,PNG,MP4,MP3)
* Dont upload any `confidential` file (Wallet keys & personal docs)
* You can upload any videos or large file too
* Replace `PRIVATE_KEY` with your actual one (Without 0x)
* Replace `RPC_URL` with your selected Network

<img width="1038" height="211" alt="481822238-a3a29264-ea9e-4872-9b4a-b7bf01a64b35" src="https://github.com/user-attachments/assets/f94c6784-8e0b-429e-82f0-ded7a1a7015b" />


### How t Get File Path in ur Local PC

To Enter Ur WSL or Ubuntu Folder
```
explorer.exe .
```
Check ur File Name & Path
```
ls -a
```


---
---

### Parameters & Their Usage

| Option         | Description                                                                              |           
|----------------|------------------------------------------------------------------------------------------|
| `-n`           | The network to check, `mainnet` or `devnet`, defaults to `mainnet`.                      |
| `-t`           | The [token](https://docs.irys.xyz/build/d/features/supported-tokens) to use when funding.|
| `-w`           | Your private key. (without 0x)                                                           |
| `--tags`       | Tags to include, format `<file_name> <file_format>`.                                     |
| `--provider-url` | RPC URL to use.   [FROM_HERE](https://chainlist.org/)                                  |

---

## 🔶For Next Day Run This Command

#1 Open WSL and Put this Command 

- Put Directly 7️⃣ Number Command

## Delete Irys Storage Node
```
sudo npm uninstall -g @irys/cli
```
