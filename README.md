## NFT Marketplace with Rust on Solana

### Compile and Deploy Contracts
- make sure you are working on a Linux Distro
- If you have windows installed, make sure you have WSL installed. Either in WSL, or Linux:
  - make sure you have solana installed
  - make sure you have rust installed
  - install phantom wallet on the browser or any from the list
  - make sure u have a solana wallet with SOL token (devnet)
  - Config to devnet

- [Configuring Rust and Solana on WSL](https://medium.com/nerd-for-tech/how-to-setup-windows-subsystem-linux-with-visual-studio-code-on-windows-10-b06fdbe9b30b)

```
solana config set --url devnet
```
- Create wallet
```
solana-keygen new
```
- Add test token to the wallet

```
solana airdrop 5
```
navigate to the rust folder
```
cd program
```
build the project
```
cargo build-bpf
```
- After the build step completes, deploy the program to devnet
```
solana program deploy ./path/to/the_program.so -u devnet
```
- Clear client/packages/web/.env variables to create of a fresh new store

- start the app
```
cd ../client/packages
yarn && yarn bootstrap
yarn start
```

### Open the site in a browser 

```
http://localhost:3000
```
- Now connect wallet
- Create NFT
- Sell NFT
