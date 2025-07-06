# Contributing to ReflexVault™

Thank you for your interest in contributing to ReflexVault™! This document provides guidelines and information for contributors.

## Code of Conduct

We are committed to providing a welcoming and inspiring community for all. Please read and follow our [Code of Conduct](./CODE_OF_CONDUCT.md).

## How to Contribute

### Reporting Issues

Before creating an issue, please:
1. Check if the issue already exists
2. Use the issue template
3. Provide detailed reproduction steps
4. Include relevant logs and screenshots

### Suggesting Features

We welcome feature suggestions! Please:
1. Check existing feature requests
2. Use the feature request template
3. Explain the use case and benefits
4. Consider implementation complexity

### Code Contributions

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/amazing-feature`)
3. **Make your changes**
4. **Add tests** for new functionality
5. **Update documentation** as needed
6. **Commit your changes** (`git commit -m 'Add amazing feature'`)
7. **Push to the branch** (`git push origin feature/amazing-feature`)
8. **Open a Pull Request**

## Development Setup

### Prerequisites

- Node.js 18+
- npm or yarn
- Git

### Local Development

```bash
# Clone your fork
git clone https://github.com/your-username/reflexvault.git
cd reflexvault

# Install dependencies
npm install

# Start development server
npm run dev

# Run tests
npm test

# Run linting
npm run lint
```

### Environment Variables

Copy `.env.example` to `.env.local` and configure:

```bash
VITE_MASSA_RPC_URL=your_massa_rpc_url
VITE_CONTRACT_ADDRESS=your_contract_address
VITE_API_BASE_URL=http://localhost:3000
```

## Coding Standards

### TypeScript Guidelines

- Use strict TypeScript configuration
- Prefer interfaces over types for object shapes
- Use meaningful variable and function names
- Add JSDoc comments for public APIs

```typescript
/**
 * Calculates the reflexive adjustment for a vault
 * @param vault - The vault to analyze
 * @param userBehavior - Recent user behavior data
 * @returns The adjustment factor (0-1)
 */
function calculateReflexAdjustment(
  vault: Vault,
  userBehavior: BehaviorData
): number {
  // Implementation
}
```

### React Guidelines

- Use functional components with hooks
- Implement proper error boundaries
- Use React.memo for performance optimization
- Follow the component structure:

```typescript
interface ComponentProps {
  // Props interface
}

export const Component: React.FC<ComponentProps> = ({ prop1, prop2 }) => {
  // Hooks
  const [state, setState] = useState();
  
  // Event handlers
  const handleClick = () => {
    // Handler logic
  };
  
  // Render
  return (
    <div>
      {/* JSX */}
    </div>
  );
};
```

### CSS/Tailwind Guidelines

- Use Tailwind utility classes
- Create custom components for repeated patterns
- Follow mobile-first responsive design
- Use semantic color names

```typescript
// Good
<button className="bg-primary-500 hover:bg-primary-600 text-white px-4 py-2 rounded-lg">
  Click me
</button>

// Avoid
<button className="bg-blue-500 hover:bg-blue-600 text-white px-4 py-2 rounded-lg">
  Click me
</button>
```

## Testing Guidelines

### Unit Tests

- Write tests for all utility functions
- Test component behavior, not implementation
- Use descriptive test names
- Aim for >90% code coverage

```typescript
describe('calculateReflexAdjustment', () => {
  it('should return 0.5 for moderate behavior changes', () => {
    const vault = createMockVault();
    const behavior = createMockBehavior({ changeLevel: 'moderate' });
    
    const result = calculateReflexAdjustment(vault, behavior);
    
    expect(result).toBe(0.5);
  });
});
```

### Integration Tests

- Test complete user workflows
- Verify API integrations
- Test error handling scenarios

### E2E Tests

- Test critical user journeys
- Verify cross-browser compatibility
- Test responsive design

## Documentation

### Code Documentation

- Document all public APIs
- Include usage examples
- Explain complex algorithms
- Keep documentation up-to-date

### User Documentation

- Write clear, step-by-step guides
- Include screenshots and examples
- Consider different user skill levels
- Test documentation with real users

## Security Guidelines

### Smart Contract Security

- Follow Rust best practices
- Implement comprehensive tests
- Use formal verification where possible
- Regular security audits

### Frontend Security

- Validate all user inputs
- Sanitize data before display
- Use secure communication protocols
- Implement proper error handling

### Wallet Integration

- Never store private keys
- Verify all transactions
- Implement proper signing flows
- Handle wallet disconnections gracefully

## Performance Guidelines

### Frontend Performance

- Optimize bundle sizes
- Implement code splitting
- Use React.memo and useMemo appropriately
- Optimize images and assets

### Smart Contract Performance

- Minimize gas usage
- Optimize storage operations
- Use efficient algorithms
- Implement batch operations

## Release Process

### Version Numbering

We follow [Semantic Versioning](https://semver.org/):
- **MAJOR**: Breaking changes
- **MINOR**: New features (backward compatible)
- **PATCH**: Bug fixes (backward compatible)

### Release Checklist

- [ ] All tests pass
- [ ] Documentation updated
- [ ] Security review completed
- [ ] Performance benchmarks met
- [ ] Changelog updated
- [ ] Version bumped
- [ ] Release notes prepared

## Community Guidelines

### Communication

- Be respectful and inclusive
- Provide constructive feedback
- Help newcomers learn
- Share knowledge and resources

### Collaboration

- Review pull requests promptly
- Provide detailed feedback
- Test others' contributions
- Celebrate successes together

## Recognition

Contributors are recognized in:
- README.md contributors section
- Release notes
- Community Discord
- Annual contributor awards

## Getting Help

### Development Questions

- **Discord**: [#development channel](https://discord.gg/reflexvault)
- **GitHub Discussions**: For longer-form discussions
- **Stack Overflow**: Tag questions with `reflexvault`

### Security Issues

For security vulnerabilities:
- **Email**: [security@reflexvault.com](mailto:security@reflexvault.com)
- **Bug Bounty**: Submit through our bug bounty program
- **Responsible Disclosure**: Follow our security policy

## Resources

### Learning Resources

- [Massa Documentation](https://docs.massa.net/)
- [React Documentation](https://reactjs.org/docs/)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)

### Development Tools

- [VS Code Extensions](./docs/DEVELOPMENT.md#vscode-extensions)
- [Debugging Guide](./docs/DEVELOPMENT.md#debugging)
- [Testing Utilities](./docs/DEVELOPMENT.md#testing)

## License

By contributing to ReflexVault™, you agree that your contributions will be licensed under the MIT License.

---

Thank you for contributing to ReflexVault™! Together, we're building the future of autonomous DeFi. 🚀