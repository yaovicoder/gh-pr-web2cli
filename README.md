# gh-pr-web2cli

A Bash CLI tool to export GitHub Pull Request diffs, inline review comments, review threads, and PR metadata—mirroring the content and context of the GitHub web UI, but structured for terminal and offline code review.

## Features
- Exports a PR’s code diff with all inline review comments and threads
- Includes general PR comments, review summaries, and metadata
- Supports plain text, markdown, and HTML output
- Designed for terminal-based and offline review workflows
- No need to use the GitHub web UI for full review context

## Requirements
- Bash 4+
- [gh CLI](https://cli.github.com/)
- [git](https://git-scm.com/)
- [jq](https://stedolan.github.io/jq/)

## Usage
```bash
./gh-pr-web2cli.sh <PR_NUMBER> [options]
```
Options:
- `-o, --output DIR`     Output directory (default: current directory)
- `-f, --format FORMAT`  Output format: txt, md, html (default: txt)
- `-v, --verbose`        Enable verbose output
- `-h, --help`           Show help

## Example
```bash
./gh-pr-web2cli.sh 42 -f md -o ./reports
less ./reports/pr_42_annotated_diff.md
```

## Vision
See [VISION.md](./VISION.md) for the project vision and goals.

## License
MIT 