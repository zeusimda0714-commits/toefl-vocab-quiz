# Code Refactoring Assistant

Refactor $ARGUMENTS in this TOEFL vocabulary app following vanilla JavaScript best practices.

## Task

I'll help you refactor code by:

1. Analyzing the current implementation in index.html or quiz.html
2. Identifying improvement opportunities
3. Applying modern vanilla JS patterns
4. Maintaining existing functionality
5. Ensuring Firebase integrations still work

## Process

1. Read the relevant section of the HTML file
2. Identify code smells, duplication, or outdated patterns
3. Plan the refactoring strategy
4. Implement changes while maintaining behavior
5. Verify Firebase Auth and Firestore operations still work

## Refactoring Techniques for This Project

- Extract repeated logic into reusable functions
- Convert callbacks to async/await for Firebase operations
- Improve DOM manipulation patterns (use textContent for XSS safety)
- Simplify complex conditionals in quiz logic
- Better event delegation instead of per-element listeners
- Improve error handling for Firebase operations
- Organize code sections with clear comments
- Extract inline styles to CSS classes where beneficial

## Important Notes

- This is a vanilla JS app — no frameworks or build tools
- All code lives in HTML files with embedded scripts
- Firebase is loaded via CDN ES modules
- Do not introduce npm dependencies or build tooling
- Keep the single-file structure unless explicitly asked to split
- Test changes by opening the file in a browser