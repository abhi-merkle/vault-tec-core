## Compiling this project

#### Step 1
```
npm cache clean --force
# delete the .yarn or node_modules folder if needed
npm install
```

#### Step 2
change compiler version to 0.8.8 in hardhat.config.ts

#### Step 3
change `pragma solidity 0.8.7; -> pragma solidity ^0.8.7;` in all the files

#### Step 4
create .env file and set MNEMONIC and INFURA_API_ENDPOINT keys there

#### Step 5
npx hardhat compile

#### Step 6
```
forge init --no-git --no-commit --vscode --force
```

#### Step 7
set src = "contracts" in foundry.toml

#### Step 8
set solc_version = "0.8.8" in foundry.toml

#### Step 9
set remappings.txt as follows
```
@ensdomains/=node_modules/@ensdomains/
@openzeppelin/=node_modules/@openzeppelin/
eth-gas-reporter/=node_modules/eth-gas-reporter/
hardhat/=node_modules/hardhat/
forge-std/=lib/forge-std/src/
```

#### Step 10
run `forge build` to build the whole project
