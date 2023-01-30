<p align="center" height='100px'>
  <img width="200" height="auto" src="https://user-images.githubusercontent.com/78480857/215549241-ce4b1e08-9715-4920-afac-08afb65b9f73.jpeg">
  <br>
  <br>
  Muon Testnet(ALICE)
</p>

# Requirements
## Hardware

|  Component | Recommended |
| ------------ | ------------ |
| CPU  | Dual-Core  |
| RAM | DDR4 4 GB  |
| Disk  | 20 GB  |
| Connection | 1000MBps Bandwith |


## Software

| Component | Min. Requirements |
| ------------ | ------------ |
| OS |  Ubuntu 18.04 or higher | 


# Dependencies
## Install Docker
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```
# 1. Run the Node
## Clone the Repository
```
git clone https://github.com/muon-protocol/muon-node-js.git --recurse-submodules --branch testnet
```

## Build the Node
```
cd muon-node-js
docker-compose build
```

## Now run the node using docker
```
docker-compose up -d
```

# 2. Check your Node
**If this is run successfully, the node's status can be viewed by opening the following address in your browser:** 
```
http://<server-ip>:8000/status
```
<br>
<br>
**The result should look like this:**
<br>
![image](https://user-images.githubusercontent.com/78480857/215552389-6478c7c7-b635-44d2-8e9b-43ba3bc88471.png)

# 3. Adding Node to the Network
![image](https://user-images.githubusercontent.com/78480857/215552593-588f6a05-e3cc-4473-bbe9-4ec4f18fde97.png)
go to https://alice.muon.net/join.
<br>
1. Connect your wallet 
2. Switch Network to BSC Testnet
3. Mint Faucet (Need BSC Testnet as fees. request here:https://testnet.bnbchain.org/faucet-smart)
4. Approve to spend the token
5. Stake the token to your Node (Fill Node address and peerID with yours that displayed on step 2 before)
<br>
<br>
<br>
**Now Check again your Node, it should being Online:**
```
http://<server-ip>:8000/status
```
![image](https://user-images.githubusercontent.com/78480857/215553662-0bf40a6b-9487-4e68-a5c2-ae5cf907f0d2.png)

