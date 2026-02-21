# Assess Pronunciation

Evaluate English pronunciation quality from audio recordings.

## When to Use

Use this skill when the user wants to:
- Check how well they pronounced a word, phrase, or sentence
- Get detailed feedback on specific sounds (phonemes)
- Identify pronunciation weaknesses

## How It Works

1. User provides audio (file or recording) and the text they spoke
2. The `assess_pronunciation` tool scores at four levels:
   - **Overall** (0-100): Composite quality score
   - **Sentence** (0-100): Fluency and connected speech
   - **Word** (0-100): Per-word accuracy
   - **Phoneme** (0-100): Individual sound accuracy in IPA and ARPAbet
3. Results include confidence score and audio quality metrics

## Usage

```
User: "Check my pronunciation of 'The quick brown fox jumps over the lazy dog'"
→ Record or upload audio, then call assess_pronunciation with the audio and text
→ Review scores and identify weak phonemes
→ Suggest practice words using minimal pairs
```

## Tips

- Audio must be clear (SNR > 15dB) — quiet environment recommended
- Supported formats: WAV, MP3, OGG, WebM
- Audio duration: 0.5s to 60s
- The `get_phoneme_inventory` tool lists all 39 English phonemes the scorer evaluates
