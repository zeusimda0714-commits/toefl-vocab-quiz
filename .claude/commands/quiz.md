# Quiz Logic Assistant

Help with quiz functionality for $ARGUMENTS in this TOEFL vocabulary app.

## Task

I'll help with quiz-related features by:

1. Analyzing the quiz logic in index.html
2. Understanding the 4 quiz types and their scoring
3. Fixing quiz bugs or adding new quiz features
4. Ensuring wrong words are tracked correctly
5. Verifying data flows to/from Firestore

## Quiz Types

1. **Type 1** — Korean to English meaning (multiple choice)
2. **Type 2** — English word to Korean meaning (multiple choice)
3. **Type 3** — English spelling practice (type the word)
4. **Type 4** — Matching words with definitions

## Data Structure

- Words organized by day (1-30) in `words_data.js` and `all_days_data.js`
- Each word has: word, synonyms, Korean meaning
- Distractors are generated from same part-of-speech words

## Common Quiz Issues

- Wrong answer counting not matching actual mistakes
- Score display inconsistencies
- Distractor generation picking too-similar options
- Wrong words not saving to Firestore correctly
- Quiz state not resetting properly between attempts
- Day selection not loading correct word set

## Important Notes

- Quiz logic is embedded in index.html JavaScript
- Test quiz flows manually in the browser
- Check Firestore for saved wrong words after quiz completion
- Verify scoring across all 4 quiz types independently