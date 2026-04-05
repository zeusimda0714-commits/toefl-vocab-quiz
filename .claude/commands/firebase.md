# Firebase Assistant

Help with Firebase operations for $ARGUMENTS in this TOEFL vocabulary app.

## Task

I'll help with Firebase Auth and Firestore operations by:

1. Analyzing the current Firebase integration in index.html
2. Identifying issues with auth flows or Firestore queries
3. Implementing new Firebase features
4. Optimizing Firestore reads/writes
5. Improving error handling for Firebase operations

## Firebase Setup in This Project

- Firebase v12.11.0 loaded via CDN ES modules
- Project: `the-toefl-lab`
- Services: Firebase Auth (email/password) + Cloud Firestore
- No Firebase CLI or npm packages — all client-side

## Common Tasks

### Authentication
- Email/password signup and login
- User profile management (displayName)
- Session persistence with `setPersistence`
- Auto-logout after inactivity

### Firestore Operations
- Reading/writing user quiz progress
- Storing wrong words per user
- User profile data
- Cross-device data sync

### Best Practices
- Always use try/catch with async Firebase operations
- Check `auth.currentUser` before Firestore operations
- Use `onAuthStateChanged` for reactive auth state
- Batch Firestore writes when updating multiple documents
- Use `merge: true` for partial document updates

## Important Notes

- Firebase SDK is loaded from CDN, not npm
- API keys in client code are normal for Firebase (security comes from Firestore rules)
- Test auth flows in browser; check Firestore data in Firebase Console
- Be mindful of Firestore read/write quotas on the free tier