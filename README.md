# voicetomd

Transcribe meeting audio into tidy markdown notes

Built for my own use; public in case it helps someone.

## What it does

- Batch mode for a folder of recordings
- Segments grouped into 5-minute sections
- Outputs markdown with timestamps you can skim
- Local whisper, no API key needed

## Install

```bash
pip install -r requirements.txt
# needs ffmpeg installed
```

## Examples

```bash
python transcribe.py meeting.mp3
# -> meeting.notes.md
```

## Project structure

```text
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   └── workflows/
│       └── ci.yml
├── docs/
│   ├── configuration.md
│   └── development.md
├── examples/
│   └── quickstart.md
├── tests/
│   └── test_smoke.py
├── .gitignore
├── CHANGELOG.md
├── SECURITY.md
├── requirements.txt
└── transcribe.py
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```

## Changelog

- `0.1.1` - fix edge case in argument parsing
- `0.1.0` - first working version
