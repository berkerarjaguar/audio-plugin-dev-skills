# Audio Plugin Dev Skills

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) plugin marketplace that provides skills for validating audio plugins across formats (VST3, AudioUnit, CLAP). Once installed, you can ask Claude to validate your plugins or use the slash commands directly in Claude Code.

## Installation

In Claude Code, run:

```
/plugin marketplace add iPlug3/audio-plugin-dev-skills
/plugin install audio-plugin-validators@audio-plugin-dev-skills
```

## Skills

### audio-plugin-validators

Validate VST3, AudioUnit, and CLAP plugins using official and third-party CLI tools.

| Skill | Description |
|-------|-------------|
| `validate-audiounit` | Validate AudioUnit v2/v3 plugins with `auval` |
| `validate-vst3` | Validate VST3 plugins with Steinberg's validator |
| `validate-clap` | Validate CLAP plugins with `clap-validator` |
| `validate-pluginval` | Validate VST3/AU plugins with pluginval |
| `validate-vst3-editorhost` | Test VST3 UI with EditorHost |
| `check-codesign` | Check macOS code signature, hardened runtime, entitlements, and notarization |

You can invoke these as slash commands (e.g. `/audio-plugin-validators:validate-vst3`) or just ask Claude to "validate my VST3 plugin" and it will use the appropriate skill.

### Requirements

- **auval**: Included with macOS
- **VST3 validator**: Build from [VST3 SDK](https://github.com/steinbergmedia/vst3sdk) or use pre-built
- **clap-validator**: [Download](https://github.com/free-audio/clap-validator/releases) or build with Cargo
- **pluginval**: [Download](https://github.com/Tracktion/pluginval/releases)

## License

Copyright (c) 2026 Oli Larkin

MIT
