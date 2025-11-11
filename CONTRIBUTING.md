# Contributing to Crypto Analyzer Ultimate

First off, thank you for considering contributing to Crypto Analyzer Ultimate! 🎉

It's people like you that make this tool better for the entire crypto trading community.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Setup](#development-setup)
- [Pull Request Process](#pull-request-process)
- [Coding Standards](#coding-standards)
- [Commit Messages](#commit-messages)

---

## Code of Conduct

This project and everyone participating in it is governed by our Code of Conduct. By participating, you are expected to uphold this code. Please report unacceptable behavior to the project maintainers.

**Our Standards:**
- ✅ Be respectful and inclusive
- ✅ Welcome newcomers and help them learn
- ✅ Focus on what is best for the community
- ✅ Show empathy towards other community members
- ❌ No harassment, trolling, or insulting comments
- ❌ No spam or self-promotion
- ❌ No sharing of private information

---

## How Can I Contribute?

### 🐛 Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates.

**When creating a bug report, include:**
- **Clear title** describing the issue
- **Steps to reproduce** the bug
- **Expected behavior** vs actual behavior
- **Screenshots** if applicable
- **Environment details:**
  - Browser (Chrome, Firefox, etc.)
  - Operating System
  - Docker version (if using Docker)

**Example:**
```markdown
**Title:** Alert not sending when confluence is 3/3

**Description:**
When all 3 timeframes show LONG signal, Telegram alert is not sent.

**Steps to Reproduce:**
1. Configure BTC on 5m, 1h, 4h
2. Wait for 3/3 confluence
3. No alert received

**Expected:** Alert should be sent
**Actual:** No alert

**Environment:**
- Chrome 119
- Windows 11
- Telegram bot configured correctly
```

### 💡 Suggesting Features

Feature suggestions are welcome! Please provide:
- **Clear feature description**
- **Use case** - Why is this useful?
- **Expected behavior** - How should it work?
- **Optional:** Implementation ideas

**Example:**
```markdown
**Feature:** Volume-weighted moving average (VWMA)

**Use Case:** 
VWMA gives more weight to high-volume periods, providing better trend signals than SMA.

**How It Should Work:**
- Add VWMA calculation alongside SMA
- Display in chart with different color
- Include in signal generation

**Implementation Ideas:**
- Calculate VWMA in technical indicators section
- Add toggle in settings to enable/disable
```

### 🔧 Contributing Code

1. **Fork** the repository
2. **Create a branch** for your feature: `git checkout -b feature/amazing-feature`
3. **Make your changes**
4. **Test thoroughly**
5. **Commit** with clear messages: `git commit -m 'feat: add amazing feature'`
6. **Push** to your fork: `git push origin feature/amazing-feature`
7. **Open a Pull Request**

---

## Development Setup

### Prerequisites
- Git installed
- Text editor (VS Code recommended)
- Web browser (Chrome/Firefox)
- (Optional) Docker for testing

### Setup Steps

```bash
# 1. Fork and clone
git clone https://github.com/YOUR-USERNAME/crypto-analyzer-ultimate.git
cd crypto-analyzer-ultimate

# 2. Create a branch
git checkout -b feature/my-new-feature

# 3. Make changes
# Edit index.html

# 4. Test locally
python3 -m http.server 8080
# Open http://localhost:8080

# 5. Or test with Docker
docker-compose up -d
# Open http://localhost:8080
```

### Project Structure

```
crypto-analyzer-ultimate/
├── index.html              # Main application (React standalone)
├── docker-compose.yml      # Docker configuration
├── README.md               # Main documentation
├── LICENSE                 # MIT License
├── CHANGELOG.md            # Version history
├── CONTRIBUTING.md         # This file
└── docs/                   # Additional documentation
    ├── INSTALLATION.md
    ├── TELEGRAM-SETUP.md
    └── ADX-GUIDE.md
```

---

## Pull Request Process

### Before Submitting

- ✅ Test your changes thoroughly
- ✅ Ensure no console errors
- ✅ Check responsive design (mobile/desktop)
- ✅ Update documentation if needed
- ✅ Add comments to complex code
- ✅ Follow coding standards

### PR Template

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Testing
How did you test this?

## Screenshots (if applicable)
Add screenshots here

## Checklist
- [ ] Code follows style guidelines
- [ ] Tested thoroughly
- [ ] Documentation updated
- [ ] No console errors
```

### Review Process

1. Maintainer will review your PR
2. Feedback may be requested
3. Make requested changes
4. Once approved, PR will be merged
5. Your contribution will be credited!

---

## Coding Standards

### JavaScript/React

```javascript
// ✅ Good: Clear function names
const calculateRSI = (prices, period = 14) => {
  // Implementation
};

// ❌ Bad: Unclear names
const calc = (p, n) => {
  // Implementation
};

// ✅ Good: Comments for complex logic
// Calculate True Range for ADX
const tr = Math.max(
  high - low,
  Math.abs(high - prevClose),
  Math.abs(low - prevClose)
);

// ✅ Good: Consistent formatting
const signal = {
  type: 'LONG',
  confidence: 'High',
  indicators: {...}
};
```

### Styling

```javascript
// ✅ Use Tailwind utility classes
className="bg-white/10 rounded-xl p-6 hover:bg-white/20"

// ✅ Responsive design
className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4"
```

### Comments

```javascript
// ✅ Good comments explain WHY
// Use 0.998 multiplier to place SL slightly below support
// This prevents stop-hunting and gives wiggle room
const stopLoss = supportPrice * 0.998;

// ❌ Bad comments state WHAT (obvious from code)
// Multiply by 0.998
const stopLoss = supportPrice * 0.998;
```

---

## Commit Messages

Follow [Conventional Commits](https://www.conventionalcommits.org/) format:

### Format
```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `perf`: Performance improvements
- `test`: Adding tests
- `chore`: Maintenance tasks

### Examples

```bash
# Good commits
git commit -m "feat: add ADX indicator to technical analysis"
git commit -m "fix: telegram alerts not sending for SHORT signals"
git commit -m "docs: update installation guide with Docker steps"
git commit -m "perf: optimize S/R calculation for large datasets"

# With body
git commit -m "feat: add volume-weighted moving average

- Calculate VWMA using price and volume
- Add toggle in settings to enable/disable
- Display in chart with orange color
- Include in signal scoring system"
```

---

## Documentation

When adding features, update relevant documentation:

### Code Documentation
```javascript
/**
 * Calculate ADX (Average Directional Index)
 * Measures trend strength from 0-100
 * 
 * @param {Array} klines - OHLCV candlestick data
 * @param {number} period - Calculation period (default: 14)
 * @returns {Object} ADX data with strength and direction
 */
const calculateADX = (klines, period = 14) => {
  // Implementation
};
```

### README Updates
- Add new features to Features section
- Update screenshots if UI changed
- Add configuration steps if needed

### Changelog
- Add entry to CHANGELOG.md
- Follow Keep a Changelog format
- Link to relevant PRs/issues

---

## Questions?

- **Issues:** [GitHub Issues](https://github.com/YOUR-USERNAME/crypto-analyzer-ultimate/issues)
- **Discussions:** [GitHub Discussions](https://github.com/YOUR-USERNAME/crypto-analyzer-ultimate/discussions)
- **Email:** your-email@example.com

---

## Recognition

Contributors will be recognized in:
- README.md acknowledgments section
- CHANGELOG.md for their specific contributions
- GitHub contributors page

---

**Thank you for contributing! 🚀**

Every contribution, no matter how small, helps make this project better for everyone.

Happy coding! 💻
