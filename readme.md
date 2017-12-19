# Ethereum Simple Contract Example

Ethereum simple contract example where contract creator allows some people in the network to send 
money. This example is based on [Truffle framework](http://truffleframework.com), which is just a
convenient tool to organize workflow with Ethereum contracts and launch test network emulator.

Setup
-----

To set up *development server*, you need to have [NodeJS v8+](https://nodejs.org) installed. Then,
do the following:

```bash
git clone https://github.com/ZitRos/ethereum-simple-contract-example.git
cd ethereum-simple-contract-example
npm install
npm run test # OR
npm run win-test
```

Q&A
---

❓ What happens when you assign `-1` to a `uint`?

✔️Implicit IDE warning shows up. But, by using `uint(-1)`, all the 32 bits of `uint` type flip 
and this results to a number `2^32 - 1`, which is `4294967295`.

❓ What happens when you assign a `uint256` of the value `5` to a variable type `uint8`?

✔️It will still be `5`, as `5` ∈ `uint8` ∈ `uint256`.

❓ What happens when Strings of different lengths are assigned? Does it cost more gas? Why?

✔️Yes, it does cost more gas, as [docs say](https://github.com/ethereum/wiki/wiki/Design-Rationale).
There are a gas price per every byte and per every operation on EVM.

❓ What does the `_` do in function modifiers?

✔️The code for the function being modified is inserted where the `_` is placed in the modifier. We can add
more than one `_`s in the modifier code. And the code of the function being modified is inserted in each
place where `_` is located in the modifier.

❓ How many Wei are one Finney?

✔️`1 * 10^15` Wei.
