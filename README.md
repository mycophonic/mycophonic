# Mycophonic

> High-fidelity audio, from the ground up

![Mycophonic](logo.jpg)

Mycophonic is a modular, open source platform for building music management and playback applications. Audiophile-grade. Pure Go.

The stack spans ALSA/CoreAudio interfaces, multi-room streaming, library management, and UI components.

---

## Projects

Note that everything is currently under heavy development.

We will update this table as projects graduate.

As of 2026/01/30, this is for hard-boiled developers only, sorry!

| Project                                                          | Public? | Maturity  | Description                                                       |
|------------------------------------------------------------------|---------|-----------|-------------------------------------------------------------------|
| [agar](https://github.com/mycophonic/agar)                       | ✔       | α         | Test infrastructure and audio file generation                     |
| [cordyceps](https://github.com/mycophonic/cordyceps)             | ✘       | α         | LLM infrastructure                                                |
| [flac](https://github.com/mycophonic/flac)                       | ✔       | 0.1.0-dev | Optimized fork of https://github.com/mewkiz/flac                  |
| [TBD](https://github.com/mycophonic/PLACEHOLDER)                 | ✘       | α         | ?                                                                 |
| [gill](https://github.com/mycophonic/gill)                       | ✘       | α         | Metadata extraction and tagging                                   |
| [haustorium](https://github.com/mycophonic/haustorium)           | ✔       | α         | PCM analysis and defect detection (clipping, silence, DC offset)  |
| [homebrew-mycota](https://github.com/mycophonic/homebrew-mycota) | ✔       | 0.1.0-dev | Homebrew formulas for binaries                                    |
| [hypha](https://github.com/mycophonic/hypha)                     | ✘       | α         | Library management, file organization, online metadata lookups    |
| [mycelium](https://github.com/mycophonic/mycelium)               | ✘       | α         | Network playback: multi-room sync, zones, device federation       |
| [mycophonic](https://github.com/mycophonic/mycophonic)           | ✔       | α         | This here, and the (future) website                               |
| [primordium](https://github.com/mycophonic/primordium)           | ✔       | β         | Core facilities: network defaults, filesystem helpers, formatting |
| [saprobe](https://github.com/mycophonic/saprobe)                 | ✔       | α         | Decoders: FLAC, ALAC, MP3, Ogg Vorbis (TBD: DSD, AAC, Opus)       |
| [sporeprint](https://github.com/mycophonic/sporeprint)           | ✔       | α         | Audio fingerprinting (CGO: requires Chromaprint)                  |
| [pileus](https://github.com/mycophonic/pileus)                   | ✘       | α         | User interfaces / web                                             |

---

## Tech

**Language:** Pure Go. No CGO except where OS-level access demands it (CoreAudio, ALSA, Chromaprint).

**Platforms:** macOS and Linux are first-class. Windows support planned.

**Philosophy:** Each project is a library first. Import what you need. No framework lock-in.

---

## Installation

See [homebrew-mycota](https://github.com/mycophonic/homebrew-mycota) for CLI tools.

For library usage, `go get` individual projects as needed.

---

## Why mushroom names?

Mycelium networks are decentralized, resilient, and interconnected underground systems that enable communication and resource sharing across vast distances.

That's the architecture we're building.

Also, mushrooms are cool.

To audiophilia and beyond.

---

## Manifesto

### Why new foundations?

Every media player reinvents the wheel. Decoders, taggers, library databases, streaming protocols—rebuilt from scratch,
again and again. The collective waste of effort is staggering.

We believe the core building blocks of audio software are solved problems, or should be.
They should be shared infrastructure, not proprietary silos.

### Why not contribute to existing projects?

We do, where it makes sense.

But most audio tooling was designed in the late 90s and early 2000s. It shows:
- C/C++ codebases that are difficult to integrate into modern stacks
- Architectural decisions optimized for constraints that no longer exist
- Backward compatibility baggage that prevents fundamental improvements

Mycophonic is a clean-room reimplementation with 2026 assumptions:
- Memory safety by default
- Cross-platform without #ifdef hell
- Designed for streaming-first workflows
- Modern format support (DSD, hi-res PCM, lossless codecs)
- Novel approaches where warranted (buffer-feedback clock synchronization)

### Who is this for?

- Developers building media players, music managers, or audio tools
- Tinkerers who want to understand how audio software works
- Anyone frustrated by the state of existing options

---

## License

[Apache](LICENSE) unless otherwise noted in individual projects.

---

## Contributing

Issues and PRs welcome. See individual project repos for contribution guidelines.

For architecture discussions, open an issue in the corresponding project, or right here if it does not fit in a single
project.

Also, all projects pictures have been generated by LLM...

If you are a designer or photographer, and you are interested in replacing these with something better, that would be welcome!
