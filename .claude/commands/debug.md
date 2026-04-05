# Debug Assistant

Help me debug the issue with $ARGUMENTS in this TOEFL vocabulary app.

## Task

I'll help you identify and fix the problem by:

1. Understanding the issue description
2. Analyzing the relevant section of index.html or quiz.html
3. Identifying potential causes
4. Suggesting and implementing fixes
5. Verifying the solution

## Process

1. Examine error messages or unexpected behaviors described
2. Locate the relevant code section in index.html (it's a large single-file app)
3. Analyze the code flow and potential failure points
4. Check Firebase Auth and Firestore interactions
5. Suggest specific fixes with explanations

## Common Issues in This Project

- Firebase Auth state not updating correctly
- Firestore read/write permission errors
- Quiz logic bugs (wrong answer counting, scoring)
- DOM manipulation issues (innerHTML vs textContent)
- Event listener conflicts in the single-page app
- Data loading issues with vocabulary JS files
- CSS/layout problems on mobile devices
- XSS vulnerabilities from unsanitized user input
- Async/await issues with Firebase operations

## Important Notes

- All code is in index.html and quiz.html — no separate JS modules
- Firebase is loaded via CDN ES modules, not npm
- No build step or linter — check for syntax errors manually
- Test fixes by opening index.html in a browser