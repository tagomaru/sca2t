# Sca2t (Smart Contract Audit Assistant Tool): A set of utilities for auditing Solidity contracts.

#### 

Sca2t is an assistant tool for smart contract audit. It provides an output to visualize dependencies among smart contracts and generate event declaration and its call for debug to trace which functions are called.

Sca2t pronunciation is like skˈɚːt.

## Getting Started

Install it via npm:

```shell
npm install -g sca2t
```

## Command List

### eventgen

The `eventgen` command inserts event decalaration and its call into all of the contracts and functions except view functions.
Don't forget to backup your solidity files before do this.

```shell
sca2t eventgen *.sol
```
or

```shell
find . -name "*.sol" | xargs sca2t eventgen
```


### dependencies

The `dependencies` command outputs a draggable report to visualize dependencies among contracts.
Sca2t supports dependencies of inheritance, using declaration, and user defined type.
Sca2t search local or global package for contracts
If you want to search local, run the command on your package root, otherwise this searches global ones.

```shell
sca2t dependencies contracts/TGCrowdsale.sol
```


<img src="https://raw.githubusercontent.com/wiki/tagomaru/sca2t/images/dependencies.png" height="236">

## License

GPL-3.0

