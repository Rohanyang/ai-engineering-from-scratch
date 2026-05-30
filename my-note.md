My AI engineering learning note - Rohan 26/05/30

## GPU Setup Decision

I will use Google Colab for GPU-heavy lessons.

Local WSL will be used for:
- Git and GitHub workflow
- Python basics
- API and keys
- RAG / Agent / MCP tooling
- Lightweight local scripts

Google Colab will be used for:
- PyTorch GPU tests
- Deep learning examples
- Transformer / model training experiments

Reason:
My laptop is not ideal for local CUDA setup or model training, and Colab provides a working Tesla T4 GPU without affecting local performance.
