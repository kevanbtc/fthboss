# Getting Started with FTH-G

Welcome to FTH-G! This guide will help you set up your development environment and start working with the tokenized gold platform.

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

### Required Tools
- **[Git](https://git-scm.com/)** - Version control
- **[Foundry](https://book.getfoundry.sh/)** - Ethereum development framework
- **[Node.js 18+](https://nodejs.org/)** - For tooling and scripts
- **[A Web3 Wallet](https://metamask.io/)** - MetaMask recommended

### Optional but Recommended
- **[VS Code](https://code.visualstudio.com/)** - Code editor
- **[Solidity Extension](https://marketplace.visualstudio.com/items?itemName=JuanBlanco.solidity)** - Syntax highlighting
- **[Docker](https://docker.com/)** - For containerized development

## 🚀 Quick Setup

### 1. Install Foundry
```bash
# Install Foundry
curl -L https://foundry.paradigm.xyz | bash
foundryup
```

### 2. Clone the Repository
```bash
# Clone the repository
git clone https://github.com/kevanbtc/fthboss.git
cd fthboss

# Navigate to smart contracts
cd smart-contracts/fth-gold
```

### 3. Install Dependencies
```bash
# Install smart contract dependencies
forge install

# Install specific OpenZeppelin version
forge install OpenZeppelin/openzeppelin-contracts@v5.0.2 --no-commit
```

### 4. Build the Project
```bash
# Compile smart contracts
forge build

# Check if build was successful
echo "Build completed successfully!"
```

### 5. Run Tests
```bash
# Run all tests
forge test

# Run tests with verbose output
forge test -vvv

# Run specific test file
forge test --match-path test/FTHG.t.sol
```

## 🧪 Development Workflow

### Running Tests
```bash
# Basic test run
forge test

# With gas reporting
forge test --gas-report

# With coverage
forge coverage

# Watch mode (re-run on file changes)
forge test --watch
```

### Code Formatting
```bash
# Check formatting
forge fmt --check

# Auto-format code
forge fmt
```

### Static Analysis
```bash
# Install slither
pip install slither-analyzer

# Run security analysis
slither .
```

## 🌐 Network Configuration

### Local Development
```bash
# Start local anvil node
anvil

# Deploy to local network
forge script script/Deploy.s.sol --rpc-url http://localhost:8545 --private-key <your-private-key> --broadcast
```

### Testnet Deployment
```bash
# Set environment variables
export PRIVATE_KEY="your-private-key"
export SEPOLIA_RPC_URL="https://sepolia.infura.io/v3/your-key"
export ETHERSCAN_API_KEY="your-etherscan-key"

# Deploy to Sepolia
forge script script/Deploy.s.sol --rpc-url $SEPOLIA_RPC_URL --private-key $PRIVATE_KEY --broadcast --verify
```

## 🔧 Environment Setup

### Creating .env File
```bash
# Copy example environment file
cp .env.example .env

# Edit .env with your values
nano .env
```

### Required Environment Variables
```env
# RPC URLs
MAINNET_RPC_URL=https://mainnet.infura.io/v3/YOUR_KEY
SEPOLIA_RPC_URL=https://sepolia.infura.io/v3/YOUR_KEY

# Private keys (never commit these!)
PRIVATE_KEY=your-private-key-here

# API keys
ETHERSCAN_API_KEY=your-etherscan-api-key
COINMARKETCAP_API_KEY=your-cmc-api-key

# Contract addresses (updated after deployment)
FTHG_TOKEN_ADDRESS=
STAKE_LOCKER_ADDRESS=
ORACLE_MANAGER_ADDRESS=
```

## 📚 Understanding the System

### Core Components

1. **FTHG Token** - The main tokenized gold ERC20 token
2. **StakeLocker** - Handles gold staking and receipt tokens
3. **DistributionManager** - Manages yield distributions
4. **OracleManager** - Price feed management
5. **KYCSoulbound** - Identity verification tokens

### Key Concepts

- **Gold Backing**: 1kg of physical gold per token
- **Staking Process**: 150-day lock period before conversion
- **Yield Distribution**: 10% monthly in USDT
- **KYC Compliance**: Soulbound tokens for identity verification
- **Multi-chain Support**: Ethereum, Base, Arbitrum

## 🎯 Your First Integration

### 1. Check Token Balance
```solidity
// Get FTHG balance
uint256 balance = IERC20(fthgAddress).balanceOf(userAddress);
```

### 2. Stake Gold
```solidity
// Stake 1kg of gold (1 token)
uint256 kg = 1;
uint256 maxETHCost = 0.1 ether; // Maximum ETH willing to pay

stakeOrchestrator.stakeWithETH{value: maxETHCost}(kg, maxETHCost);
```

### 3. Check Staking Status
```solidity
// Get user's staking receipt
(uint256 kg, uint256 lockEnd, bool converted) = stakeLocker.stakes(userAddress);
```

### 4. Convert After Lock Period
```solidity
// Convert stake to FTHG tokens (after 150 days)
stakeLocker.convertToFTHG();
```

## 🐛 Troubleshooting

### Common Issues

**Build Failures**
```bash
# Clean and rebuild
forge clean
forge build
```

**Test Failures**
```bash
# Run specific failing test with verbose output
forge test --match-test testFunctionName -vvvv
```

**Gas Limit Issues**
```bash
# Increase gas limit in foundry.toml
gas_limit = 30_000_000
```

**Dependency Issues**
```bash
# Reinstall dependencies
rm -rf lib/
forge install
```

### Getting Help

- **Documentation**: Check our [comprehensive docs](../README.md)
- **GitHub Issues**: [Report bugs](https://github.com/kevanbtc/fthboss/issues)
- **Community**: [GitHub Discussions](https://github.com/kevanbtc/fthboss/discussions)
- **Support**: support@fthboss.com

## 🎓 Next Steps

Once you have the basic setup working:

1. **[Integration Guide](integration.md)** - Learn how to integrate FTH-G
2. **[Testing Guide](testing.md)** - Write comprehensive tests
3. **[Deployment Guide](deployment.md)** - Deploy to production
4. **[API Documentation](../api/)** - Detailed API reference

## 📝 Best Practices

### Development
- Always run tests before committing
- Use meaningful commit messages
- Follow the coding standards
- Document your code

### Security
- Never commit private keys
- Use hardware wallets for mainnet
- Audit your contracts before deployment
- Follow security best practices

### Testing
- Aim for >95% test coverage
- Test both success and failure cases
- Use fuzz testing for edge cases
- Test gas usage and optimizations

---

**Need Help?** Join our community or reach out to our support team. We're here to help you succeed with FTH-G!