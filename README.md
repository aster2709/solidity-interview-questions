# Solidity Interview Questions

This is a questions list you can be faced with in a Solidity focused interview.

---

_Additional questions accepted via PR_

_Discalimer: This is not a complete package of questions guaranteeing you a job and is definitely incomplete. Depending on what position the candidate is applying for, the questions can be different, intuitive and also out of scope_

## Questions

**Solidity**

[Base 1]

- What is `mapping` datatype?
- default values in `mappping(address => bool)` ?
- What does `public` visibilty mean?
  - `internal` vs `private`
- `view` vs `pure`
- Have you used `openzeppelin`
- Fungible vs Non fungible
- What are modifiers?
- `memory` vs `storage`
- What are the popular token standards?
  - Whats is the purpose for each?
- What are some of the global variables?
- What is a fallback function?
- Have you used Hardhat framework?

[Base 2]

- What is variable default visibility `uint a;`
- Have you used `SafeMath`?
  - Why?
- What does `_;` in modifiers mean?
- What is assembly in solidity;
- What is `keccak256`?
- What does `abi.encodePacked` do?
- What contracts from Openzeppelin have you integrated excluding token standards?
- What is a DEX?
- What does `indexed` in events mean?
- Random number in the contract?
- `transfer` vs `send` vs `call`
- What is re-entrancy?
- What are oracles?
- What are Meta txs?
- What are upgradable contracts?

Note: _Skip moving to Base3 if the candidate's answers from Base2 are not convincing, Base3 should ideally be for senior/lead dev positions_

[Base 3]

- What is forking, how can you test an app on mainnet?
- What is `delegatecall`
  - who is `msg.sender` in a `delegatecall`?

```sh
struct S {
  uint a;
}
mapping (uint => S) map;
function setValue() external {
  S memory s = map[1] // assume a `struct S` at `1` exists
  s.a = 5;
}
function getValue() external view returns() {
  return map[1].value;
}
// what would calling `setValue() and then getValue()` give you?
```

- What is the `create2` assembly opcode?
  - How would you go about deploying a contract to a custom address
- What are proxies?
- Why can't upgradable contracts have a constructor?
- What are AMMs
- How would you generate a seemingly safe random number?
- How can cross chain bridging be implemented?
- Have you implemented royalties for an NFT?
