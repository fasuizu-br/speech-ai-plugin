# Speech Workflow

Complete pronunciation practice workflow: listen to a model pronunciation, record your attempt, get scored feedback.

## When to Use

Use this skill when the user wants to:
- Practice pronunciation with a full feedback loop
- Compare their pronunciation against a reference
- Follow a structured practice session

## Workflow Steps

### Step 1: Generate Reference Audio
Use `synthesize_speech` to create a model pronunciation of the target text.
Let the user choose from 12 English voices (American/British, male/female).

### Step 2: User Records Their Attempt
The user listens to the reference and records their own attempt.

### Step 3: Assess Pronunciation
Call `assess_pronunciation` with the user's audio and the target text.
Review scores at all levels (overall, sentence, word, phoneme).

### Step 4: Provide Feedback
- Highlight strong points (scores 80+)
- Identify weak phonemes (scores below 60)
- Suggest minimal pairs for practice
- Compare with the reference pronunciation

### Step 5: Iterate
Repeat steps 2-4 for targeted improvement.

## Example

```
User: "I want to practice saying 'particularly'"
→ 1. synthesize_speech("particularly", voice="af_heart")
→ 2. User records their attempt
→ 3. assess_pronunciation(user_audio, "particularly")
→ 4. "Your /r/ scored 45 — try 'right' vs 'light' as practice"
→ 5. User tries again
```

## Available Voices

Call `list_tts_voices` to see all 12 voices with accents and quality grades.
