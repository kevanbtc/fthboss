# Contributing to FTH-G

We love your input! We want to make contributing to FTH-G as easy and transparent as possible, whether it's:

- Reporting a bug
- Discussing the current state of the code
- Submitting a fix
- Proposing new features
- Becoming a maintainer

## Development Process

We use GitHub to host code, track issues and feature requests, and accept pull requests.

### Pull Request Process

1. Fork the repo and create your branch from `main`
2. If you've added code that should be tested, add tests
3. If you've changed APIs, update the documentation
4. Ensure the test suite passes
5. Make sure your code lints
6. Issue that pull request!

### Development Setup

1. **Prerequisites**
   ```bash
   # Install Node.js (v18+)
   # Install Foundry for smart contract development
   curl -L https://foundry.paradigm.xyz | bash
   foundryup
   ```

2. **Clone and Setup**
   ```bash
   git clone https://github.com/kevanbtc/fthboss.git
   cd fthboss
   
   # Setup smart contracts
   cd smart-contracts/fth-gold
   forge install
   ```

3. **Run Tests**
   ```bash
   # Smart contract tests
   cd smart-contracts/fth-gold
   forge test
   
   # Check coverage
   forge coverage
   ```

### Code Style Guidelines

#### Smart Contracts (Solidity)
- Follow the [Solidity Style Guide](https://docs.soliditylang.org/en/latest/style-guide.html)
- Use OpenZeppelin patterns and imports where possible
- Maintain 100% test coverage for new contracts
- Include comprehensive NatSpec documentation

#### General Guidelines
- Use clear, descriptive variable and function names
- Comment complex logic thoroughly
- Keep functions small and focused
- Follow existing patterns in the codebase

### Commit Message Guidelines

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
type(scope): description

[optional body]

[optional footer]
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

**Examples:**
```
feat(contracts): add multi-chain staking support
fix(oracle): handle stale price data correctly
docs(api): update integration examples
test(staking): add edge case coverage
```

## Reporting Bugs

We use GitHub Issues to track bugs. Report a bug by [opening a new issue](https://github.com/kevanbtc/fthboss/issues/new?template=bug_report.md).

**Great Bug Reports** include:
- A quick summary and/or background
- Steps to reproduce
- What you expected would happen
- What actually happens
- Notes (possibly including why you think this might be happening, or stuff you tried that didn't work)

## Suggesting Features

We use GitHub Issues for feature requests. Suggest a feature by [opening a new issue](https://github.com/kevanbtc/fthboss/issues/new?template=feature_request.md).

**Great Feature Requests** include:
- Clear description of the problem you're trying to solve
- Proposed solution with examples
- Consideration of alternatives
- Understanding of implementation complexity

## Security Vulnerabilities

**DO NOT** create public issues for security vulnerabilities. Instead, please follow our [Security Policy](SECURITY.md) and report security issues privately.

## Areas for Contribution

### High Priority
- **Smart Contract Security**: Security reviews and testing
- **Documentation**: API documentation, tutorials, examples
- **Testing**: Edge case coverage, integration tests
- **Tooling**: Developer experience improvements

### Medium Priority
- **Multi-Chain Support**: Additional network integrations
- **Frontend**: User interface improvements
- **Monitoring**: Observability and alerting
- **Performance**: Gas optimization

### Good First Issues
Look for issues labeled `good first issue` or `help wanted` in our [issue tracker](https://github.com/kevanbtc/fthboss/issues).

## Code Review Process

1. **Automated Checks**: All PRs must pass CI/CD checks
2. **Peer Review**: At least one maintainer review required
3. **Security Review**: Security-sensitive changes require additional review
4. **Testing**: New features must include comprehensive tests

### Review Criteria
- **Functionality**: Does the code work as intended?
- **Security**: Are there potential security vulnerabilities?
- **Performance**: Is the code efficient?
- **Maintainability**: Is the code readable and well-documented?
- **Testing**: Are there adequate tests?

## Community

### Discussions
Use [GitHub Discussions](https://github.com/kevanbtc/fthboss/discussions) for:
- General questions about the project
- Ideas and brainstorming
- Technical discussions
- Community feedback

### Code of Conduct
This project adheres to a [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## Recognition

Contributors will be recognized in:
- Git commit history
- Release notes for significant contributions
- Project documentation
- Annual contributor highlights

## License

By contributing, you agree that your contributions will be licensed under the same license as the project (MIT License).

## Getting Help

- 📖 **Documentation**: Check our [documentation](docs/)
- 💬 **Discussions**: Use GitHub Discussions for questions
- 🐛 **Issues**: Use GitHub Issues for bugs and feature requests
- 📧 **Direct Contact**: Reach out to maintainers for urgent matters

Thank you for contributing to FTH-G! 🚀