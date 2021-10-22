# Solidity Interview Questions

This is a questions list you can be faced with in a Solidity focused interview. 

---
*Additional questions accepted via PR*

*Discalimer: This is not a complete package of questions guaranteeing you a job and is definitely incomplete. Depending on what position the candidate is applying for, the questions can be different, intuitive and also out of scope*

## Questions

**Blockchain/Defi Overview** [Can be skipped in a only solidity focused interview]

- What is the essential difference between Bitcoin & Ethereum?
- What is mining?
- What is gas?
  - Why is gas needed?
- Proof of work?
  - Proof of stake?
- What is Staking?
  - Yield?
  - Flashloans?
  - Frontrunning?
- What are scaling solutions?
- Eth 2.0?

**Solidity**

[Base 1]

- What is `mapping` datatype?
- What does `public` visibilty mean?
  - `internal` vs `private`
- `view` vs `pure`
- What is `bytes`?
- What is `keccak256`?
- Fungible vs Non fungible
- `view` vs `pure`
- What is `bytes`?
- What are modifiers?
- `memory` vs `storage`
- What are the popular token standards?
  - Whats is the purpose for each?
- What is the `receive()` function?
- What is variable default visibility `uint a;`
- What frameworks have you used? - Have you written tests in typescript / using Typechain?

[Base 2]
- What does `_;` in modifiers mean?
- What is forking, how can you fork mainnet?
- What contracts from Openzeppelin have you integrated excluding token standards?
- What is a DEX?
- What does `indexed` in events mean?
- Random number in the contract?
- `transfer` vs `send` vs `call`
- What is re-entrancy?
- What are oracles?
- What are Meta txs?
- What are upgradable contracts?
- Why SafeMath?

Note: _Skip moving to Base3 if the candidate's answers from Base2 are not convincing, Base3 should ideally be for senior/lead dev positions_

[Base 3]

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
// what would calling `getValue()` give you?

```
- What is the `create2` assembly opcode?
- What are proxies?
- What are AMMs
- How would you generate a seemingly safe random number?
- How can cross chain bridging be implemented?
- Have you implemented royalties for an NFT?
