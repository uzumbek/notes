# notes

A collection of hands-on knowledge on **preparing AI-driven automation locally**
— running LLMs and AI agents on your own hardware for coding, system work, and
general automation, with no cloud dependency.

The goal is to turn "set this up on a new machine" from a fuzzy memory into a
repeatable, documented process. Each document is a real setup or fix, written up
so another developer (or future-you) can reproduce it on their own workstation.

## Topics

- **Local LLM serving** — running large models on consumer/prosumer GPUs,
  exposed as a standard API.
- **AI agents for development** — wiring an agent to a local model for coding,
  debugging, and system administration.
- **Hardware bring-up** — getting niche or new hardware (GPUs, NICs) working
  with the right drivers and workarounds.

## Documents

| Document | What it covers |
|---|---|
| [Running Qwen3.8-27B on a T7820 + R9700](qwen3.8-27b-r9700-local-llm-setup.md) | End-to-end local LLM setup: AMD Vulkan driver, prebuilt llama.cpp, GGUF model, systemd service, power cap, and wiring up the Hermes agent for coding/system work. |
| [Realtek RTL8852BE PCIe 32-bit DMA fix](realtek-rtl8852be-pcie-32bit-dma-fix.md) | Diagnosing and patching a 36-bit DMA interop bug that kept a WiFi card from creating an interface, including the kernel-module rebuild. |

## Conventions

- Documents are written for a **fresh workstation** — prerequisites, commands,
  and verification steps are included so each can be followed top to bottom.
- **No private information** (hostnames, home paths, IPs, MACs, network names)
  is committed. Paths use `~/` and portable placeholders.
- Diagrams use Mermaid where a picture clarifies the flow.

## Adding a document

1. Write it as a self-contained, reproducible guide (goal → steps → verify).
2. Redact anything identifying before committing.
3. Add a row to the **Documents** table above.
4. Commit and push.
