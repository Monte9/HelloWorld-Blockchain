# HelloWorld-Blockchain

Hello World Dapp in Ethereum with Solidity

## Beginner's Guide

### 1. Write a smart contract

Here's what a simple Hello World smart contract looks like:

```
pragma solidity ^0.4.8;

contract HelloWorld {
  uint public balance;

  function HelloWorld() {
      balance = 1000;
  }
}
```

### 2. Compile and deploy

Using `truffle`, we can compile and deploy the smart contract to our local test network using `testrpc`

```truffle compile && truffle migrate --reset```

### 3. Run the contract

Run the following commands on the `truffle console` with `testrpc` running in the background:

```
var helloworld = HelloWorld.deployed()

helloworld.then(a => console.log(a.balance().then(console.log)))
```

**Output:**

```
{ [String: '1000'] s: 1, e: 3, c: [ 1000 ] }
```

In the above output, you can see the balance (of 1000) that we had in our smart contract.

### 4. Next Steps

Build a smart contract that has the ability to read-write the balance in a smart contract.

## Resources:

- [Youtube Video - Introduction to Ethereum Smart Contract Development with Solidity](https://www.youtube.com/watch?v=8jI1TuEaTro)
- [Truffle Getting Started Guide](http://truffleframework.com/docs/getting_started/installation)
- [Testrpc Getting Started Guide](https://github.com/ethereumjs/testrpc#install)
