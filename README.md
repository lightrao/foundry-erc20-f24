# Foundry ERC20

Talk about ERC20 contract

## Requirements

- [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
  - You'll know you did it right if you can run `git --version` and you see a response like `git version x.x.x`
- [foundry](https://getfoundry.sh/)
  - You'll know you did it right if you can run `forge --version` and you see a response like `forge 0.2.0 (816e00b 2023-03-16T00:05:26.396218Z)`

## Start

- run:
  ```bash
  mkdir foundry-erc20-f24
  cd foundry-erc20-f24
  code .
  forge init
  ```

## What is an ERC? What is an EIP?

- EIP: Ethereum Improvement Proposal
- ERC: Ethereum Request for Comments
- BEP: Binance Evolution Proposal
- PEP: Python Enhancement Proposal
- go to `https://eips.ethereum.org/EIPS/eip-20`
- go to `https://ethereum.org/en/developers/docs/standards/tokens/erc-20/`

## What is an ERC20?

- ERC-20
- ERC-677
- ERC-777

## Manually Creating an ERC20 Token

- create `ManualToken.sol`

## ERC20 Token - Openzeppelin

- run
  ```bash
  forge install OpenZeppelin/openzeppelin-contracts --no-commit
  ```
- add `remappings` into `foundry.toml`
- create `OurToken.sol`
- run `forge build`

## Deploy Script

- create `DeployOurToken.s.sol`
- create `Makefile`
- run:
  ```bash
  forge install
  make anvil
  make deploy
  ```

## AI Tests

- create `OurTokenTest.t.sol`
- run:
  ```bash
  forge test --match-test testBobBalance
  ```
- go to `https://etherscan.io/tokenapprovalchecker`, we can see the amount eth `transferFrom` can use
- run:

  ```bash
  forge test --match-test testAllowancesWorks
  forge test
  forge coverage
  ```
