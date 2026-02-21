# Installation Guide for Speech AI MCP Server

## Prerequisites
- An API subscription key (get one at https://brainiall.com or via Azure Marketplace)

## Configuration

Add to your MCP settings (Claude Desktop, Cursor, Cline, etc.):

```json
{
  "mcpServers": {
    "speech-ai": {
      "url": "https://pronunciation-mcp.thankfulfield-a7857897.eastus.azurecontainerapps.io/mcp",
      "headers": {
        "Ocp-Apim-Subscription-Key": "YOUR_API_KEY"
      }
    }
  }
}
```

## Available Tools

| Tool | Description |
|------|-------------|
| `assess_pronunciation` | Score English pronunciation at phoneme, word, and sentence levels (0-100) |
| `check_pronunciation_service` | Health check for the pronunciation service |
| `get_phoneme_inventory` | List all 39 English phonemes the scorer evaluates |
| `transcribe_audio` | Transcribe audio to text with word-level timestamps |
| `check_stt_service` | Health check for the STT service |
| `synthesize_speech` | Generate speech from text with 12 English voices |
| `list_tts_voices` | List available TTS voices |
| `check_tts_service` | Health check for the TTS service |

## Quick Test

After configuration, try:
1. Ask your AI assistant to "check the pronunciation service health"
2. Record yourself saying "Hello, how are you?" and ask for a pronunciation assessment
