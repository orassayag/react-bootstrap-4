# Contributing

Contributions to this project are [released](https://help.github.com/articles/github-terms-of-service/#6-contributions-under-repository-license) to the public under the [project's open source license](LICENSE).

Everyone is welcome to contribute to this project. Contributing doesn't just mean submitting pull requests—there are many different ways for you to get involved, including answering questions, reporting issues, improving documentation, or suggesting new features.

## How to Contribute

### Reporting Issues

If you find a bug or have a feature request:
1. Check if the issue already exists in the [GitHub Issues](https://github.com/orassayag/react-bootstrap-4/issues)
2. If not, create a new issue with:
   - Clear title and description
   - Steps to reproduce (for bugs)
   - Expected vs actual behavior
   - Your environment details (OS, Node version, browser)

### Submitting Pull Requests

1. Fork the repository
2. Create a new branch for your feature/fix:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Make your changes following the code style guidelines below
4. Test your changes thoroughly
5. Commit with clear, descriptive messages
6. Push to your fork and submit a pull request

### Code Style Guidelines

This project uses:
- **React.js** for UI components
- **Bootstrap 4** for styling framework
- **SCSS** for custom styles
- **ESLint** for code quality

Before submitting:
```bash
# Install dependencies
npm install

# Start development server
npm start

# Build for production
npm build

# Run tests
npm test
```

### Coding Standards

1. **Component structure**: Use class components with PropTypes validation
2. **File organization**: Keep components in separate folders with their styles
3. **Naming conventions**: Use PascalCase for components, camelCase for functions
4. **SCSS**: Follow BEM methodology for class naming
5. **No inline styles**: Use SCSS files for styling
6. **PropTypes**: Always define propTypes for component props

### Adding New Features

When adding new features:
1. Create a new component in `src/containers/` or `src/hoc/`
2. Add corresponding SCSS file in the same folder
3. Update routing in `src/containers/App/App.jsx` if needed
4. Add to exports in `src/containers/index.js`
5. Test thoroughly in different browsers

## Questions or Need Help?

Please feel free to contact me with any question, comment, pull-request, issue, or any other thing you have in mind.

* Or Assayag <orassayag@gmail.com>
* GitHub: https://github.com/orassayag
* StackOverflow: https://stackoverflow.com/users/4442606/or-assayag?tab=profile
* LinkedIn: https://linkedin.com/in/orassayag

Thank you for contributing! 🙏
