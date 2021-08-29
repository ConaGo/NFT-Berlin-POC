## NFT POC

# setup

1. create .env file in root folder with the following variables

- API_KEY="your http api key from the project on Alchemy"
- PRIVATE_KEY="private key of the Metamask wallet"
- PUBLIC_KEY = "your-public-account-address"

The wallet needs to have funds on the tesnetwork of choice

2. compile scripts

```shell
npx hardhat compile
```

3. choose a testnetwork(ropsten here) and run the deploy script

```shell
npx hardhat run scripts/deploy.js --network ropsten
```

expected output

```shell
Contract deployed to address: 0x81c587EB0fE773404c42c1d2666b5f557C470eED
```

4. go to [Ropsten Etherscan](https://ropsten.etherscan.io/) and search for your contract adress

5. Done! Estimated cost at the time of writing was 17.5€

## Minting

1. Upload your media uing the interplanetary file system, preferably over a convinient API like [Pinata](https://www.pinata.cloud/)

2. add the resulting url with the hash code as image key in the nft-metadata.json (optionally configure additional metadata)

3. add the address of your contract in scripts/mint-nft.js

```javascript
const contractAddress = "0xa9aec7212682175fa9260c1b17531ffa36cdcee1";
```

4. run the mintNFT function with the IPFS address from Pinata ( "https://gateway.pinata.cloud/ipfs/QmYueiuRNmL4MiA2GwtVMm6ZagknXnSpQnB3z2gWbz36hP")

```shell
run node scripts/mint-nft.js
```

5. Check the transaction status on [Alchemy Mempool](https://dashboard.alchemyapi.io/mempool) or search your transaction hash on [Ropsten Etherscan](https://ropsten.etherscan.io/)

6. Done! Estimated cost 0.5€
