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
- What solidity framework do you use?
  - How familiar are you with writing test suites

[Base 2]

- What is variable default visibility `uint a;`
- Have you used `SafeMath`?
  - Why?
- What does `_;` in modifiers mean?
- What is assembly in solidity;
- What is `keccak256`?
- What does `abi.encodePacked` do?
- What contracts from Openzeppelin have you integrated excluding token standards?
- What does `indexed` in events mean?
  - how many indexed params are permitted?
```sol
contract A {}
```
- ^Can you send ether to the above contract?
- `transfer` vs `send` vs `call`
- What is re-entrancy?
- What are oracles?
- What are Meta txs?
- What are upgradable contracts?
- Have you interacted with any popular protocols programatically?
```sol
struct S {
  uint a;
}
mapping (uint => S) map;
function setValue() external {
  S memory s = map[1];
  s.a = 5;
}
function getValue() external view returns(uint256) {
  return map[1].a;
}
```
- ^What would calling `setValue() and then getValue()` return?

Note: _Skip moving to Base3 if the candidate's answers from Base2 are not convincing, Base3 should ideally be for senior/lead dev positions_

[Base 3]

- What does the memory address `0x40` point to?
- Can you change the visibility of a variable in an upgradeable contract?
- What is a `stack too deep` error and when can it occur?
  - Ways to resolve it?
- How can you simulate transactions from someone else's address? 
- What is `delegatecall`
  - Who is `msg.sender` in a `delegatecall`?
- Have you interacted with uniswap v3 oracle?
- What is the `create2` assembly opcode?
- What are proxy contracts?
- How would you generate a seemingly safe random number?
