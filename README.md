# CapaKit AI App Kits

This repository is the public registry for CapaKit AI app Kits. Each entry points to a standalone kit repository.

## Hello World

Minimal AI app Kit that exposes a single MCP tool returning hello world.

- Source: https://github.com/capakit/hello-world-demo-kit
- Run:

```sh
capakit run https://github.com/capakit/hello-world-demo-kit
```
- Skill:

```sh
capakit run https://github.com/capakit/hello-world-demo-kit --global-skill codex
```


## Kids Storybook Creator

Local-first AI app Kit for generating and editing a simple illustrated children's storybook.

- Source: https://github.com/capakit/kids-storybook-creator-demo-kit
- Run:

```sh
capakit run https://github.com/capakit/kids-storybook-creator-demo-kit \
--mount models=~/.capakit/models
```


## llama.cpp Local

Local AI app Kit that serves GGUF models through llama.cpp with OpenAI-compatible and MCP endpoints.

- Source: https://github.com/capakit/llama-cpp-local-kit
- Run:

```sh
capakit run https://github.com/capakit/llama-cpp-local-kit \
--mount models=~/.capakit/models
```
- Skill:

```sh
capakit run https://github.com/capakit/llama-cpp-local-kit --global-skill codex \
--mount models=~/.capakit/models
```


## Local Image Tagger

Local AI app Kit for tagging images from a mounted folder with a local vision model.

- Source: https://github.com/capakit/local-image-tagger-demo-kit
- Run:

```sh
capakit run https://github.com/capakit/local-image-tagger-demo-kit \
--mount images=<path-to-images> \
--mount models=~/.capakit/models
```
- Skill:

```sh
capakit run https://github.com/capakit/local-image-tagger-demo-kit --global-skill codex \
--mount images=<path-to-images> \
--mount models=~/.capakit/models
```


## Stable Diffusion Local

Local AI app Kit that serves stable-diffusion.cpp through an OpenAI-compatible image endpoint.

- Source: https://github.com/capakit/stable-diffusion-local-kit
- Run:

```sh
capakit run https://github.com/capakit/stable-diffusion-local-kit \
--mount models=~/.capakit/models
```


## Realtime Voice

Local-first AI app Kit for a browser voice conversation loop with speech recognition, local chat, and speech output.

- Source: https://github.com/capakit/realtime-voice-demo-kit
- Run:

```sh
capakit run https://github.com/capakit/realtime-voice-demo-kit \
--mount models=~/.capakit/models
```


