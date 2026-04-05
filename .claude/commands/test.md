# Manual Testing Guide

Help test $ARGUMENTS in this TOEFL vocabulary app.

## Task

Since this project has no automated testing framework, I'll help by:

1. Identifying what needs to be tested for the given feature
2. Providing manual test steps to verify in the browser
3. Reviewing code paths for edge cases and potential bugs
4. Checking Firebase Auth and Firestore error scenarios
5. Suggesting defensive code improvements

## Testing Areas

### Quiz Logic
- Verify correct/wrong answer counting across all 4 quiz types
- Check score calculation and display
- Test edge cases: empty word lists, single word, all correct, all wrong
- Verify wrong words are saved correctly to Firestore

### Authentication
- Test signup flow (email/password, nickname)
- Test login/logout cycle
- Verify auto-logout after inactivity
- Test session persistence across page refreshes

### Data Sync
- Verify quiz progress saves to Firestore
- Test cross-device data loading
- Check behavior when offline or Firestore unavailable

### UI/UX
- Test responsive layout on mobile and desktop
- Verify all navigation and sidebar functionality
- Check font loading (SUITE, Paperlogy)
- Test keyboard accessibility

## Important Notes

- Open index.html in browser to test manually
- Use browser DevTools Console to check for errors
- Use Firebase Console to verify Firestore data
- Test in both Chrome and Safari for compatibility