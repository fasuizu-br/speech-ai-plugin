# Transcribe Audio

Convert spoken English audio into text with word-level timestamps.

## When to Use

Use this skill when the user wants to:
- Transcribe an audio recording to text
- Get word-level timestamps from a recording
- Check what was said in an audio file

## How It Works

1. User provides audio (file or base64-encoded)
2. The `transcribe_audio` tool returns:
   - Full transcript text
   - Per-word timestamps (start/end in seconds)
   - Per-word confidence scores (0-1)
   - Audio quality metrics

## Usage

```
User: "Transcribe this audio file"
→ Encode audio as base64
→ Call transcribe_audio
→ Present the transcript with timestamps
```

## Tips

- Supported formats: WAV, MP3, OGG, FLAC, WebM
- Audio duration: 0.5s to 120s
- Clean audio produces better results (SNR > 15dB)
- Short utterances (< 30s) work best
