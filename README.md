# DAO-IPCI contracts for Everscale

Install `everdev` and `tonos-cli`:
> Everdev must be installed globally.
```
npm i -g everdev
everdev tonos-cli install
```
> **Troubleshooting**: if you get `EACCES permissions errors` error check this [article](https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally).

Clone the repo and install dependicies:

```
git clone https://github.com/Multi-Agent-io/dao-ipci-everscale
cd dao-ipci-everscale
npm install
```
---
Generate account with following command:
```
tonos-cli genphrase
```
Copy `locklift.config-example.ts` to `locklift.config.ts` and add the generated seed to line 63. 

Building contracts: 
```
npx locklift build
```
To work with local network use Everscale Simple Emulator. To launch and stop it run:

```
everdev se start
everdev se stop
```
respectively.
To reset the network run
```
everdev se reset
```

Test contracts:
```
npx locklift test --network local
```

Deploy AssetFactory:
```
npx locklift run --network local --script scripts/1-deploy-assetFactory.ts
```
---
### Contracts on Devnet
#### AssetFactory
> 0:05e30bf3eae57adf9f5b6e45d4f55ffbb0dbf6e9b8d7441a67167631ce2675eb
