# Speech AI Plugin

Speech processing suite for AI coding assistants. Pronunciation assessment, speech-to-text, and text-to-speech — all via MCP.

## What It Does

- **Pronunciation Assessment**: Score English pronunciation at phoneme, word, and sentence levels (0-100). Exceeds human inter-annotator agreement.
- **Speech-to-Text**: Transcribe English audio with word-level timestamps and confidence scores. Sub-300ms latency.
- **Text-to-Speech**: Generate natural speech with 12 English voices (American and British). Speed control 0.5x-2.0x.

## Installation

### Claude Code
```bash
/plugin install speech-ai
```

### Cursor
```
/add-plugin speech-ai
```

### Manual (any MCP client)
Add to your MCP settings:
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

## Get an API Key

Visit [brainiall.com](https://brainiall.com) or subscribe via [Azure Marketplace](https://azuremarketplace.microsoft.com).

## Skills

| Skill | Description |
|-------|-------------|
| `assess-pronunciation` | Evaluate pronunciation quality from audio |
| `transcribe-audio` | Convert audio to text with timestamps |
| `speech-workflow` | Full practice loop: listen, record, score, improve |

## Agent

- **pronunciation-tutor**: Interactive pronunciation coaching agent with structured practice sessions

## Support

- Email: fasuizu@brainiall.com
- Website: https://brainiall.com

## License

Plugin configuration files: MIT. The Speech AI API is a proprietary commercial service.
