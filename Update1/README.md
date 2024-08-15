
# Allora Node Updated Guide For OLD Users

<p align="center">
<img src='https://github.com/BidyutRoy2/Allora-Network-Worker-Guide/blob/main/FundRaise.jpg' width='700'>
<a href="https://goreportcard.com/badge/github.com/allora-network/allora-chain">
    <img src="https://goreportcard.com/badge/github.com/allora-network/allora-chain">
</a>
</p>


## Requirements

- You must need WSL/VPS for running Allora Node
- You can buy from PQHisting : [Register Here](https://pq.hosting/?from=557648)

## System Requirements

|                |       Minimum            |       Recommended            |
|----------------|--------------------------|------------------------------|
| **RAM**        | 2 GB RAM                 | 4 GB+ RAM                   |
| **CPU Cores**  | 1 CPU cores              | 4+ CPU cores                 |
| **Disk Space** | 5 GB free disk space    | 50 GB+ free disk space (SSD) |
| **Operating System** | Ubuntu 22.04       | Ubuntu 22.04                 |


## Create Wallet & Request Faucet

- Install : [Keplr Extension](https://chrome.google.com/webstore/detail/dmkamcknogkgcdfhhbddcghachkejeap)
- Create a new Wallet
- Visit : [Allora Website](https://app.allora.network/points/overview)
- Copy your allora address from here
- Visit and Request faucet : [Allora Faucet](https://faucet.testnet-1.testnet.allora.network/)
- If there is an error, try 3-5 times

## Deployment

- Open termius/putty/WSL terminal
- Paste these 2 commands one by one


```
cd $HOME && cd basic-coin-prediction-node
```

```
sudo docker compose down -v
```

```
sudo docker stop $(docker ps -aq) 2>/dev/null
```

```
sudo docker rm $(docker ps -aq) 2>/dev/null
```

```
sudo docker rmi -f $(docker images -aq) 2>/dev/null
```

```
cd $HOME
```

```
sudo rm -rf basic-coin-prediction-node
```

```
git clone https://github.com/allora-network/basic-coin-prediction-node
```

```
cd basic-coin-prediction-node
```

```
nano config.json
```

## Edit Code NotePad & Enter ("Keplr Wallet Seed Phrase")

```
{
    "wallet": {
        "addressKeyName": "testkey",
        "addressRestoreMnemonic": "Keplr Wallet Seed Phrase",
        "alloraHomeDir": "",
        "gas": "1000000",
        "gasAdjustment": 1.0,
        "nodeRpc": "https://sentries-rpc.testnet-1.testnet.allora.network/",
        "maxRetries": 1,
        "delay": 1,
        "submitTx": false
    },
    "worker": [
        {
            "topicId": 1,
            "inferenceEntrypointName": "api-worker-reputer",
            "loopSeconds": 5,
            "parameters": {
                "InferenceEndpoint": "http://inference:8000/inference/{Token}",
                "Token": "ETH"
            }
        },
        {
            "topicId": 2,
            "inferenceEntrypointName": "api-worker-reputer",
            "loopSeconds": 5,
            "parameters": {
                "InferenceEndpoint": "http://inference:8000/inference/{Token}",
                "Token": "ETH"
            }
        },
        {
            "topicId": 7,
            "inferenceEntrypointName": "api-worker-reputer",
            "loopSeconds": 5,
            "parameters": {
                "InferenceEndpoint": "http://inference:8000/inference/{Token}",
                "Token": "ETH"
            }
        }
    ]
}
```

## Save File - ``CTRL+X`` Then ``Y`` Then Hit ``ENTER`` BUTTON


```
chmod +x init.config
./init.config
```

```
docker compose up --build
```

### Wait For Download Complete 100% & Don't Close This Terminal If You Use WSL

## Open New Terminal & Run Code


```
cd basic-coin-prediction-node
```

```
docker compose ps
```

```
docker compose logs -f worker
```
## Don't Close This Terminal If You Use WSL


## Restart Node - If VPS/WSL PC Shutdown

```
cd basic-coin-prediction-node
```

```
sudo docker compose up -d
```

```
docker ps
```


# ▄︻デ𝙂𝙚𝙩 𝙇𝙖𝙩𝙚𝙨𝙩 𝘼𝙞𝙧𝙙𝙧𝙤𝙥𝙨 & 𝙐𝙥𝙙𝙖𝙩𝙚𝙨═━一

### ▄︻デ𝙅𝙤𝙞𝙣 𝙏𝙚𝙡𝙚𝙜𝙧𝙖𝙢═━一 [🎀  𝐻𝒾𝒹𝒹𝑒𝓃 𝒢𝑒𝓂  🎀](https://t.me/hiddengemnews) 

### ░▒▓█►─═  𝓗𝓲𝒹ᗪ𝓔η Ǥέ𝕄 ═─◄█▓▒░
