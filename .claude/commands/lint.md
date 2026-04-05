# Code Review Assistant

Review and fix code quality issues in $ARGUMENTS for this TOEFL vocabulary app.

## Task

Since this project has no linter or build tools, I'll manually review code for:

1. JavaScript syntax errors and typos
2. XSS vulnerabilities (innerHTML with user data)
3. Undefined variable references
4. Unused variables and dead code
5. Firebase security issues
6. Accessibility problems
7. Browser compatibility concerns

## Process

1. Read the specified code section
2. Check for common JavaScript pitfalls
3. Verify Firebase operations have proper error handling
4. Check DOM manipulation for XSS safety
5. Look for accessibility issues in HTML structure
6. Report findings and apply fixes

## Common Issues to Check

- `innerHTML` used with user-provided data (use `textContent` instead)
- Missing `null` checks on DOM queries (`querySelector` results)
- Firebase operations without try/catch
- Missing `await` on async Firebase calls
- Event listeners not cleaned up
- Hardcoded strings that should be constants
- Console.log statements left in production code
- Missing ARIA attributes on interactive elements

## Important Notes

- No ESLint, Prettier, or TypeScript available — all review is manual
- Focus on the embedded JavaScript in HTML files
- This is a static site — no Node.js runtime issues to worry about