# Sample Hardhat Project

This project demonstrates a basic Hardhat use case. It comes with a sample contract, a test for that contract, and a Hardhat Ignition module that deploys that contract.

Try running some of the following tasks:

```shell
npx hardhat help
npx hardhat test
REPORT_GAS=true npx hardhat test
npx hardhat node
npx hardhat ignition deploy ./ignition/modules/Lock.ts
```

# Keccak CLI App

A command-line interface (CLI) application built with Deno and Hardhat, utilizing the Keccak hash function.

## Overview

This project is a simple CLI app that demonstrates the use of the Keccak hash function in a real-world scenario. It uses Deno as the runtime environment and Hardhat as the development environment.

## Features

- **Keccak Hash Function**: The project utilizes the Keccak hash function to perform cryptographic operations.
- **Deno**: The project is built using Deno, a modern runtime environment for JavaScript and TypeScript.
- **Hardhat**: The project uses Hardhat, a development environment for Ethereum smart contracts, to compile and deploy contracts.

## Use Cases

- **Cryptographic Operations**: The project can be used to perform cryptographic operations, such as hashing and verification, using the Keccak hash function.
- **Smart Contract Development**: The project can be used as a starting point for developing Ethereum smart contracts using Hardhat.
- **Deno Development**: The project demonstrates the use of Deno as a runtime environment for building CLI applications.

## Configuration

The project uses the following configuration files:

### deno.json

```json
{
  "nodeModulesDir": "auto",
  "tasks": {
    "start": "deno run cli-app/main.ts",
    "abi-gen": "deno run -RW abi/script.ts",
    "compile": "hardhat compile && deno run abi-gen",
    "vars-set": "deno run -A --node-modules-dir npm:hardhat vars set"
  },
  "imports": {
    "@cliffy/table": "jsr:@cliffy/table@1.0.0-rc.7",
    "@nomicfoundation/hardhat-toolbox-viem": "npm:@nomicfoundation/hardhat-toolbox-viem@^3.0.0",
    "@nomicfoundation/hardhat-ignition": "npm:@nomicfoundation/hardhat-ignition@^0.15.7",
    "@nomicfoundation/hardhat-viem": "npm:@nomicfoundation/hardhat-viem@^2.0.5",
    "@cliffy/command": "jsr:@cliffy/command@1.0.0-rc.7",
    "hardhat": "npm:hardhat@^2.22.15",
    "viem": "npm:viem@^2.21.38"
  }
}
```
