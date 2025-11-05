# Foundry Lottery

A decentralized lottery smart contract built using **Solidity** and **Foundry**, where participants enter the lottery by paying an entrance fee. After the lottery round ends, a random winner is selected, and the entire prize pool is transferred to them.

---

## Features

- Users can enter the lottery by sending ETH  
- Stores and tracks all participants for each round  
- Random winner selection (can plug into VRF or custom randomness logic)  
- Automatically transfers prize pool to the winner  
- Complete testing with Foundry (unit + fuzz + integration tests)  
- Scripts for deployment and interaction

---

## 🛠 Stack Used

| Component        | Technology |
|------------------|------------|
| Language         | Solidity   |
| Development      | Foundry (forge, cast, anvil) |
| Testing          | Forge test framework |
| Script Execution | forge script |

---

## Project Structure

```
FOUNDRY_LOTTERY/
│
├── src/
│   └── Lottery.sol             # Main lottery smart contract
│
├── script/
│   ├── DeployLottery.s.sol     # Deployment script
│   └── Interact.s.sol          # Optional automation & interaction script
│
├── test/
│   └── LotteryTest.t.sol       # Test cases (unit + fuzz + integration)
│
└── foundry.toml
```

---

## ⚙️ Setup

### Install Foundry

```sh
curl -L https://foundry.paradigm.xyz | bash
foundryup
```

### Install dependencies (if any)

```sh
forge install
```

---

## 🚀 Commands

### Compile

```sh
forge build
```

### Run Tests

```sh
forge test
```

Verbose mode:

```sh
forge test -vvvv
```

### Local Deployment (Anvil)

Start a local blockchain:

```sh
anvil
```


## 🔒 Security Notes

- Ensure randomness source is secure (use Chainlink VRF for production)
- Validate entrance fee to prevent spam entries
- Consider adding owner or DAO governance for upgrades

---

## 📄 License

MIT — open for modification and reuse.
