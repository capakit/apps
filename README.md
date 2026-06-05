# CapaKit Apps Registry

Run local AI apps with one CapaKit command.

This repository is the public registry for CapaKit AI app Kits. Each app is a standalone GitHub repository you can run, inspect, clone, or adapt. The registry is generated from kit-owned metadata, so the README stays human-friendly while `apps.json` stays machine-friendly.

- Machine-readable registry: [apps.json](apps.json)

## Featured Apps

### Kids Storybook Creator

<img src="assets/screenshots/kids-storybook-creator-demo-kit/screenshot.png" alt="Kids Storybook Creator screenshot" width="780">

Local-first AI app Kit for generating and editing a simple illustrated children's storybook.

**Technologies**

- web-ui
- llama.cpp
- stable-diffusion
- image-generation
- local-ai
- react
- vite
- typescript
- bun

<details>
<summary>Run and details</summary>

<p><img src="assets/screenshots/kids-storybook-creator-demo-kit/screenshot.png" alt="Kids Storybook Creator screenshot" width="640"></p>

**What it does**

- Turns a story idea into a 10-page story arc.
- Uses a local language model for story text and a local image model for page art.
- Serves a browser UI for editing pages and printing the final storybook.

**Technologies**

- web-ui
- llama.cpp
- stable-diffusion
- image-generation
- local-ai
- react
- vite
- typescript
- bun

**Run**

```sh
capakit run https://github.com/capakit/kids-storybook-creator-demo-kit \
--mount models=~/.capakit/models
```

**Source:** [kids-storybook-creator-demo-kit](https://github.com/capakit/kids-storybook-creator-demo-kit)

</details>

### Local Image Tagger

<img src="assets/screenshots/local-image-tagger-demo-kit/screenshot.png" alt="Local Image Tagger screenshot" width="780">

Local AI app Kit for tagging images from a mounted folder with a local vision model.

**Technologies**

- web-ui
- vision
- image-tagging
- llama.cpp
- mcp
- local-ai
- react
- vite
- typescript
- bun

<details>
<summary>Run and details</summary>

<p><img src="assets/screenshots/local-image-tagger-demo-kit/screenshot.png" alt="Local Image Tagger screenshot" width="640"></p>

**What it does**

- Lists images from a read-only local folder.
- Tags selected images with a bundled local vision model dependency.
- Exposes both a browser UI and an MCP image-tagging tool.

**Technologies**

- web-ui
- vision
- image-tagging
- llama.cpp
- mcp
- local-ai
- react
- vite
- typescript
- bun

**Run**

```sh
capakit run https://github.com/capakit/local-image-tagger-demo-kit \
--mount images=<path-to-images> \
--mount models=~/.capakit/models
```

**Install as a Codex skill**

```sh
capakit run https://github.com/capakit/local-image-tagger-demo-kit --global-skill codex \
--mount images=<path-to-images> \
--mount models=~/.capakit/models
```

**Source:** [local-image-tagger-demo-kit](https://github.com/capakit/local-image-tagger-demo-kit)

</details>

### Realtime Voice

<img src="assets/screenshots/realtime-voice-demo-kit/screenshot.png" alt="Realtime Voice screenshot" width="780">

CapaKit AI app Kit for a browser voice conversation loop with speech recognition, local chat, and speech output.

**Technologies**

- web-ui
- websocket
- voice
- audio
- speech-to-text
- text-to-speech
- llama.cpp
- transformers.js
- whisper
- kokoro
- local-ai
- react
- vite
- typescript
- bun

<details>
<summary>Run and details</summary>

<p><img src="assets/screenshots/realtime-voice-demo-kit/screenshot.png" alt="Realtime Voice screenshot" width="640"></p>

**What it does**

- Streams microphone audio from the browser to a CapaKit workload.
- Transcribes speech with a local Whisper model.
- Generates assistant replies through a bundled local llama.cpp dependency.
- Speaks replies with a local Kokoro TTS model.

**Technologies**

- web-ui
- websocket
- voice
- audio
- speech-to-text
- text-to-speech
- llama.cpp
- transformers.js
- whisper
- kokoro
- local-ai
- react
- vite
- typescript
- bun

**Run**

```sh
capakit run https://github.com/capakit/realtime-voice-demo-kit \
--mount models=~/.capakit/models
```

**Source:** [realtime-voice-demo-kit](https://github.com/capakit/realtime-voice-demo-kit)

</details>

## Available Apps

Expand an app for the exact command, longer description, and source repository.

<details>
<summary><strong>Hello World</strong> - Minimal AI app Kit that exposes a single MCP tool returning hello world.</summary>

**What it does**

- Starts one Bun workload with an MCP endpoint.
- Provides a tiny tool that is useful for validating CapaKit installation and skill wiring.

**Technologies**

- mcp
- starter
- typescript
- bun

**Run**

```sh
capakit run https://github.com/capakit/hello-world-demo-kit
```

**Install as a Codex skill**

```sh
capakit run https://github.com/capakit/hello-world-demo-kit --global-skill codex
```

**Source:** [hello-world-demo-kit](https://github.com/capakit/hello-world-demo-kit)

</details>

<details>
<summary><strong>Kids Storybook Creator</strong> - Local-first AI app Kit for generating and editing a simple illustrated children's storybook.</summary>

<p><img src="assets/screenshots/kids-storybook-creator-demo-kit/screenshot.png" alt="Kids Storybook Creator screenshot" width="640"></p>

**What it does**

- Turns a story idea into a 10-page story arc.
- Uses a local language model for story text and a local image model for page art.
- Serves a browser UI for editing pages and printing the final storybook.

**Technologies**

- web-ui
- llama.cpp
- stable-diffusion
- image-generation
- local-ai
- react
- vite
- typescript
- bun

**Run**

```sh
capakit run https://github.com/capakit/kids-storybook-creator-demo-kit \
--mount models=~/.capakit/models
```

**Source:** [kids-storybook-creator-demo-kit](https://github.com/capakit/kids-storybook-creator-demo-kit)

</details>

<details>
<summary><strong>llama.cpp Local</strong> - Local AI app Kit that serves GGUF models through llama.cpp with OpenAI-compatible and MCP endpoints.</summary>

**What it does**

- Downloads and runs a llama.cpp release on demand.
- Loads a local path or Hugging Face GGUF model spec.
- Exposes OpenAI-compatible chat and an MCP tool for local model prompts.

**Technologies**

- llama.cpp
- gguf
- oaic
- mcp
- local-ai
- typescript
- bun

**Run**

```sh
capakit run https://github.com/capakit/llama-cpp-local-kit \
--mount models=~/.capakit/models
```

**Install as a Codex skill**

```sh
capakit run https://github.com/capakit/llama-cpp-local-kit --global-skill codex \
--mount models=~/.capakit/models
```

**Source:** [llama-cpp-local-kit](https://github.com/capakit/llama-cpp-local-kit)

</details>

<details>
<summary><strong>Local Image Tagger</strong> - Local AI app Kit for tagging images from a mounted folder with a local vision model.</summary>

<p><img src="assets/screenshots/local-image-tagger-demo-kit/screenshot.png" alt="Local Image Tagger screenshot" width="640"></p>

**What it does**

- Lists images from a read-only local folder.
- Tags selected images with a bundled local vision model dependency.
- Exposes both a browser UI and an MCP image-tagging tool.

**Technologies**

- web-ui
- vision
- image-tagging
- llama.cpp
- mcp
- local-ai
- react
- vite
- typescript
- bun

**Run**

```sh
capakit run https://github.com/capakit/local-image-tagger-demo-kit \
--mount images=<path-to-images> \
--mount models=~/.capakit/models
```

**Install as a Codex skill**

```sh
capakit run https://github.com/capakit/local-image-tagger-demo-kit --global-skill codex \
--mount images=<path-to-images> \
--mount models=~/.capakit/models
```

**Source:** [local-image-tagger-demo-kit](https://github.com/capakit/local-image-tagger-demo-kit)

</details>

<details>
<summary><strong>Stable Diffusion Local</strong> - Local AI app Kit that serves stable-diffusion.cpp through an OpenAI-compatible image endpoint.</summary>

**What it does**

- Downloads and runs stable-diffusion.cpp on demand.
- Loads a local path or Hugging Face diffusion model spec.
- Exposes an OpenAI-compatible image-generation API for other Kits.

**Technologies**

- stable-diffusion
- image-generation
- oaic
- local-ai
- typescript
- bun

**Run**

```sh
capakit run https://github.com/capakit/stable-diffusion-local-kit \
--mount models=~/.capakit/models
```

**Source:** [stable-diffusion-local-kit](https://github.com/capakit/stable-diffusion-local-kit)

</details>

<details>
<summary><strong>Realtime Voice</strong> - CapaKit AI app Kit for a browser voice conversation loop with speech recognition, local chat, and speech output.</summary>

<p><img src="assets/screenshots/realtime-voice-demo-kit/screenshot.png" alt="Realtime Voice screenshot" width="640"></p>

**What it does**

- Streams microphone audio from the browser to a CapaKit workload.
- Transcribes speech with a local Whisper model.
- Generates assistant replies through a bundled local llama.cpp dependency.
- Speaks replies with a local Kokoro TTS model.

**Technologies**

- web-ui
- websocket
- voice
- audio
- speech-to-text
- text-to-speech
- llama.cpp
- transformers.js
- whisper
- kokoro
- local-ai
- react
- vite
- typescript
- bun

**Run**

```sh
capakit run https://github.com/capakit/realtime-voice-demo-kit \
--mount models=~/.capakit/models
```

**Source:** [realtime-voice-demo-kit](https://github.com/capakit/realtime-voice-demo-kit)

</details>
