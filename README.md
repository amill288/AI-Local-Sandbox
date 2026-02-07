# MiniCPM-o-4.5-Multimodal-Chatbot
MiniCPM-o-4.5 Multimodal Chatbot




MiniCPM-V Multimodal Chatbot (12GB-Friendly)

A local, GPU-efficient multimodal chatbot built around MiniCPM-V-4.5, supporting text, image understanding, voice input, offline text-to-speech, and optional image generation — all runnable on a single 12GB GPU.

This project focuses on practical multimodal interaction while keeping memory usage under control through careful model loading, CPU/GPU separation, and optional components.

Features

💬 Text chat with MiniCPM-V

🖼️ Image understanding (vision + language)

🎤 Speech-to-text (offline, CPU-based Whisper)

🔊 Text-to-speech (offline Piper TTS)

🔁 Audio reversal & volume control

🎨 Optional text-to-image generation (Stable Diffusion Turbo)

⚡ 12GB-GPU friendly design

🧠 No external APIs required (fully local)

Architecture Overview

MiniCPM-V-4.5 (INT4)

Runs on GPU via device_map="auto"

Speech-to-Text

faster-whisper on CPU (keeps GPU free)

Text-to-Speech

Piper (offline ONNX voice model)

Image Generation (Optional)

Stable Diffusion Turbo

Loaded on CPU and moved to GPU only during inference

UI

Gradio Blocks interface

This separation allows smooth interaction even on consumer GPUs.

Requirements
Hardware

NVIDIA GPU with ~12GB VRAM (tested)

CPU capable of running Whisper + Piper

Software

Python 3.10+

CUDA-enabled PyTorch

Linux recommended (WSL2 works well)








## License

This project is licensed under the MIT License.

Note: This repository provides a wrapper and UI for third-party models and tools.
Model weights and external dependencies are governed by their own respective licenses.
