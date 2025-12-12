# Contributing to Clinic Slot Booking System

Thank you for your interest in contributing! This document provides guidelines and instructions for contributing to the project.

## Code of Conduct

This project adheres to a Code of Conduct. By participating, you are expected to uphold this code. Please report unacceptable behavior to the project maintainers.

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check the issue list as you might find out that you don't need to create one. When you are creating a bug report, please include as many details as possible:

- **Use a clear and descriptive title**
- **Describe the exact steps to reproduce the problem**
- **Provide specific examples** (screenshots, code snippets)
- **Describe the behavior you observed** and what you expected instead
- **Include environment details** (OS, Node.js version, browser, etc.)

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, please include:

- **Use a clear and descriptive title**
- **Provide a step-by-step description** of the suggested enhancement
- **Provide specific examples** to demonstrate the steps
- **Describe the current behavior** and explain which behavior you expected to see instead
- **Explain why this enhancement would be useful**

### Pull Requests

1. **Fork the repository** and create your branch from `main`
2. **Make your changes** following our coding standards
3. **Add tests** for new functionality
4. **Ensure all tests pass** (`npm test`)
5. **Update documentation** as needed
6. **Submit a pull request** with a clear description

### Development Process

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/clinic-slot-booking.git
   cd clinic-slot-booking
   ```

2. **Install dependencies:**
   ```bash
   # Backend
   cd backend && npm install
   
   # Frontend
   cd ../frontend && npm install
   ```

3. **Create a branch:**
   ```bash
   git checkout -b feature/your-feature-name
   ```

4. **Make your changes** and test them

5. **Commit your changes:**
   ```bash
   git commit -m "feat: add your feature description"
   ```

6. **Push to your fork:**
   ```bash
   git push origin feature/your-feature-name
   ```

7. **Open a Pull Request**

## Coding Standards

### TypeScript

- Use TypeScript strict mode
- Define explicit types for function parameters and return values
- Avoid `any` type
- Follow the existing code style

### Code Style

- Use 2 spaces for indentation
- Use single quotes for strings
- Maximum line length: 100 characters
- Always use semicolons
- Follow the existing naming conventions

See [docs/coding-style.md](docs/coding-style.md) for detailed guidelines.

### Commit Messages

Follow [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation changes
- `style:` Code style changes
- `refactor:` Code refactoring
- `test:` Adding or updating tests
- `chore:` Maintenance tasks

Example:
```
feat(booking): add seat selection with visual highlighting
```

## Testing

- Write tests for new features
- Ensure all existing tests pass
- Maintain or improve test coverage
- Test edge cases and error scenarios

## Documentation

- Update README.md if needed
- Add JSDoc comments for public APIs
- Update API documentation
- Keep code comments up to date

## Questions?

If you have questions, please:
1. Check existing issues and discussions
2. Open a new issue with the `question` label
3. Contact the maintainers

Thank you for contributing! 🎉
