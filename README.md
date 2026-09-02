<div align="center">

# Rafael D. Coelho

**Independent researcher.** From-scratch machine learning, and open tooling for the Brazilian financial system.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![On-device](https://img.shields.io/badge/runs%20on-a%20laptop%20CPU-555)

Every repository below is public, runs offline where it can, and states what it does **not** prove.

</div>

## Research — machine learning built by hand

| Project | What it is | Proof you can run |
| :-- | :-- | :-- |
| **[PersonaCore](https://github.com/RAFAELDCOELHO/PersonaCore)** | A from-scratch 13.9M-parameter GPT — tokenizer, decoder, training loop, LoRA and EWC all hand-written in PyTorch — where personalization lives in the weights, not a database. Includes an adversarial privacy audit of what LoRA memory reveals under black-box attack, and a selective-erasure attempt whose failure is published in full. | `make demo` → streaming story demo on a laptop CPU. Slim checkpoint: [`m1-demo-v1`](https://github.com/RAFAELDCOELHO/PersonaCore/releases/tag/m1-demo-v1) |
| **[tensorforge](https://github.com/RAFAELDCOELHO/tensorforge)** | A deep learning framework from scratch: scalar autograd, NumPy tensors, Transformer primitives, full training loop. A real, already-trained GPT checkpoint was retrained on it and the numbers match PyTorch forward and backward — not a reimplementation validated against itself. | Parity tests against PyTorch |
| **[personacore-np](https://github.com/RAFAELDCOELHO/personacore-np)** | Inference engine for the same 13.9M GPT in pure NumPy, with optional MLX on Apple GPU. No PyTorch at serve time. | `make infer` → downloads the public checkpoint and runs the parity suite |

## Brazilian finance — SDKs and infrastructure

| Project | What it is | Status |
| :-- | :-- | :-- |
| **[brazilfi](https://github.com/RAFAELDCOELHO/brazilfi)** | Unified Python SDK for Brazilian financial-market APIs: Bacen, IBGE and Tesouro Direto behind one library, one API. | [![PyPI](https://img.shields.io/pypi/v/brazilfi.svg?label=PyPI)](https://pypi.org/project/brazilfi/) MIT |
| **[rfbcalc](https://github.com/RAFAELDCOELHO/rfbcalc)** | Typed Python client for Receita Federal's **official** CBS/IBS consumption-tax calculator. Wraps the government engine; invents no tax rules. | [![PyPI](https://img.shields.io/pypi/v/rfbcalc.svg?label=PyPI)](https://pypi.org/project/rfbcalc/) MIT |
| **[pix-billing](https://github.com/RAFAELDCOELHO/pix-billing)** | PIX-native billing API for LatAm SaaS: subscriptions, dunning, signed webhooks, valid BR-Code QR payloads. Async, type-safe, FastAPI. | Sandbox mode · MIT |
| **[autonomous-hedge-fund](https://github.com/RAFAELDCOELHO/autonomous-hedge-fund)** | Multi-agent LLM trading research on emerging markets, extending TradingAgents with a Macro Economist agent. Ships **BrazilBench**: offline classical baselines on frozen B3 splits. | `make bench` — no API key, no LLM · Apache-2.0 |

## Also

- **[atena-lang](https://github.com/RAFAELDCOELHO/atena-lang)** — a teaching language with no punctuation noise that transpiles to real Python 3, for people who have never programmed. [atena-lang.org](https://atena-lang.org)

<div align="center">

<sub>Zero-budget, on-device, reproducible: fixed seeds, pre-registered gates, and negative results published alongside the positive ones.</sub>

</div>
