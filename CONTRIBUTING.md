# Contributing to FTH-G

Thank you for your interest in contributing to the FTH-G tokenized gold platform! This document provides guidelines and information for contributors.

## 🌟 Ways to Contribute

### 💻 Code Contributions
- Bug fixes and improvements
- New features and enhancements
- Performance optimizations
- Documentation improvements

### 🐛 Bug Reports
- Security vulnerabilities (see [SECURITY.md](SECURITY.md))
- Functional issues
- Performance problems
- Documentation errors

### 💡 Feature Requests
- New functionality proposals
- User experience improvements
- Integration suggestions

## 🚀 Getting Started

### Prerequisites
- [Foundry](https://book.getfoundry.sh/getting-started/installation) for smart contract development
- Node.js 18+ for tooling and scripts
- Git for version control

### Setup Development Environment
```bash
# Clone the repository
git clone https://github.com/kevanbtc/fthboss.git
cd fthboss

# Install smart contract dependencies
cd smart-contracts/fth-gold
forge install

# Build contracts
forge build

# Run tests
forge test
```

## 🔄 Development Workflow

### 1. Fork and Clone
1. Fork the repository on GitHub
2. Clone your fork locally
3. Add the upstream remote: `git remote add upstream https://github.com/kevanbtc/fthboss.git`

### 2. Create a Branch
```bash
git checkout -b feature/your-feature-name
# or
git checkout -b fix/your-bug-fix
```

### 3. Make Changes
- Write clear, maintainable code
- Follow existing code style and conventions
- Add tests for new functionality
- Update documentation as needed

### 4. Test Your Changes
```bash
# Run smart contract tests
cd smart-contracts/fth-gold
forge test

# Run coverage analysis
forge coverage

# Check code formatting
forge fmt --check
```

### 5. Commit and Push
```bash
git add .
git commit -m "feat: add your feature description"
git push origin feature/your-feature-name
```

### 6. Create Pull Request
1. Go to your fork on GitHub
2. Click "New Pull Request"
3. Fill out the PR template
4. Wait for review and address feedback

## 📝 Code Standards

### Smart Contracts
- Follow [Solidity Style Guide](https://docs.soliditylang.org/en/latest/style-guide.html)
- Use OpenZeppelin contracts where applicable
- Include comprehensive NatSpec documentation
- Maintain high test coverage (>90%)

### Commit Messages
Follow [Conventional Commits](https://www.conventionalcommits.org/):
```
feat: add new staking mechanism
fix: resolve oracle price staleness issue
docs: update deployment guide
test: add integration tests for redemption
```

### Code Review Criteria
- **Functionality**: Does the code work as intended?
- **Security**: Are there any security vulnerabilities?
- **Performance**: Is the code efficient?
- **Maintainability**: Is the code readable and well-structured?
- **Testing**: Are there adequate tests?
- **Documentation**: Is the code properly documented?

## 🔒 Security Guidelines

### Reporting Security Issues
- **DO NOT** create public issues for security vulnerabilities
- Follow our [Security Policy](SECURITY.md)
- Contact security@fthboss.com for sensitive issues

### Security Best Practices
- Always use the latest stable versions of dependencies
- Follow smart contract security best practices
- Run security analysis tools before submitting
- Consider gas optimization impacts on security

## 🧪 Testing Guidelines

### Test Coverage Requirements
- New features must include comprehensive tests
- Bug fixes must include regression tests
- Maintain overall coverage above 90%

### Test Types
- **Unit Tests**: Test individual functions/contracts
- **Integration Tests**: Test contract interactions
- **End-to-End Tests**: Test complete user flows
- **Security Tests**: Test attack vectors and edge cases

## 📚 Documentation Standards

### Code Documentation
- All public functions must have NatSpec comments
- Complex logic should include inline comments
- README files for new modules/features

### User Documentation
- Update relevant documentation for user-facing changes
- Include examples and usage instructions
- Keep documentation up-to-date with code changes

## 🎯 Issue Guidelines

### Creating Issues
- Use appropriate issue templates
- Provide clear, detailed descriptions
- Include reproduction steps for bugs
- Add relevant labels and assignees

### Issue Labels
- `bug`: Something isn't working
- `enhancement`: New feature or request
- `documentation`: Improvements or additions to docs
- `good first issue`: Good for newcomers
- `help wanted`: Extra attention is needed
- `security`: Security-related issues

## 🤝 Community Guidelines

### Code of Conduct
All contributors must follow our [Code of Conduct](CODE_OF_CONDUCT.md).

### Communication Channels
- **GitHub Issues**: Bug reports and feature requests
- **GitHub Discussions**: General questions and discussions
- **Discord**: Real-time community chat (link in README)

### Recognition
Contributors will be recognized in:
- Release notes for significant contributions
- Contributor credits in documentation
- Special recognition for security discoveries

## 📄 License

By contributing to FTH-G, you agree that your contributions will be licensed under the same license as the project (MIT License).

## ❓ Questions?

If you have questions about contributing, please:
1. Check existing documentation and issues
2. Ask in GitHub Discussions
3. Contact the maintainers via email

Thank you for helping make FTH-G better! 🚀