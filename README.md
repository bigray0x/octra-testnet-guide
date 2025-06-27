# octra-testnet-guide
![Image 6-27-25 at 1 58 PM](https://github.com/user-attachments/assets/3401901e-f403-4675-9954-5aee248794dc)


### Octra is a blockchain network focused on Fully Homomorphic Encryption (FHE) which raised $4M, offering cryptographic tools for secure mathematical operations in isolated execution environments.

### Prerequisites :

- PC - Ubuntu needed : installation guide here - [read this article](https://x.com/bigray0x/status/1938208586070388803)
- VPS - Ubuntu is pre-nstalled : VPS purchase guide - [read this guide too](https://x.com/bigray0x/status/1938208586070388803)

### Step 1 - update system and install requirements 

```
apt install -y sudo
sudo apt update && sudo apt upgrade -y
sudo apt install -y curl git build-essential
```

- Install bun and reload profile 

```
curl -fsSL https://bun.sh/install | bash
source /root/.bashrc
``` 

- Or manually add Bun to PATH (if needed):

```
export PATH="$HOME/.bun/bin:$PATH"
```

### Step 2 - clone the wallet generator page 


```
git clone https://github.com/octra-labs/wallet-gen.git
cd wallet-gen
```

- Install project requirements

```
bun install
```

If it says bun not found run this ```“source /root/.bashrc”```

If it complains about missing packages like tweetnacl, install manually:

```
bun add tweetnacl
```

### Step 3 - Allow port in UFW
```
sudo ufw allow 8888
```

### Step 4 - start the wallet generator 

```
bun wallet_generator.ts
```


### Step 5 - generate keys and save them

- Go to - Local machine: http://localhost:8888

 ![Image 6-27-25 at 2 16 PM](https://github.com/user-attachments/assets/16e005eb-7d55-4172-8bf5-98f62c210cb5)


- Replace (localhost with your pc/vps ip address)

Once the site opens click on generate wallet.

Scroll upwards and copy the first 4 details the most important.

![IMG_3787](https://github.com/user-attachments/assets/55a964c3-5ef0-43dd-83a6-470143a6b8b1)








