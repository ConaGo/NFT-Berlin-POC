## NFT POC

# setup

1. create .env file in root folder with the following variables

API_KEY="your http api key from the project on Alchemy"
PRIVATE_KEY="private key of the Metamask wallet"

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
