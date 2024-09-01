# Nillion-Node


## Cấu hình yêu cầu chạy node
```
Operating System : Ubuntu 22.04
CPU : Minimum of 1/2 core
RAM : 4 GB
Storage : SSD or NVMe with at least 100GB of space
Bandwidth: 100Mbps.
```

## 1. RUN NODE
```
sudo apt update && sudo apt upgrade -y

sudo apt install screen -y

screen -S nillionGA

sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin -y

docker pull nillion/retailtoken-accuser:v1.0.0

mkdir -p nillion/accuser

```
## 2. Show Account ID
```
docker run -v ./nillion/accuser:/var/tmp nillion/retailtoken-accuser:v1.0.0 initialise

```

## 3. Show Address & Private key
```
  sudo cat /root/nillion/accuser/credentials.json

2️⃣Save the all Private,Pub Keys

3️⃣import the Private key into Keplr wallet

4️⃣And go here to Claim Nillion Faucet: https://faucet.edgenet.allora.network/

5️⃣Once you get the Nillion Testnet Tokens


```
## 4. Now go to Verifier Page
```![image](https://github.com/user-attachments/assets/76cb2700-d664-4280-8714-69dce9ba515f)

Wallet connect to web: https://verifier.nillion.com/secrets


1️⃣Secret 1: Image of handpalm
2️⃣Secret 2: Nillion wallet address
![image](https://github.com/user-attachments/assets/6fd1ff01-220c-4596-af6f-0b29743000ac)

3️⃣ verifier: Account ID & PUB_KEY (##2..... , ## 3.....)
![image](https://github.com/user-attachments/assets/83be4d01-fcbb-4c38-a489-aafd2f9b6df9)
```
## 5. Runing Node
```
docker run -v ./nillion/accuser:/var/tmp nillion/retailtoken-accuser:v1.0.0 accuse --rpc-endpoint "https://testnet-nillion-rpc.lavenderfive.com" --block-start 5243311
```
## 6. Check Node Active 
```
https://verifier.nillion.com/verifier

```

