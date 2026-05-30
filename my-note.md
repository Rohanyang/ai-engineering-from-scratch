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
My Colab GPU is Tesla T4 with about 15GB VRAM.

Using the fp16 rule of thumb:
1 parameter ≈ 2 bytes

15GB / 2 bytes ≈ 7.5B parameters

So in theory, this GPU can fit around a 7B fp16 model's weights.
In practice, because inference also needs memory for activations, KV cache, and framework overhead, a safer estimate is smaller than 7B for fp16, or around 7B if using quantization such as 4-bit.
My Colab GPU is Tesla T4 with about 15GB VRAM.

Using the fp16 rule of thumb:
1 parameter ≈ 2 bytes

15GB / 2 bytes ≈ 7.5B parameters

So in theory, this GPU can fit around a 7B fp16 model's weights.
In practice, because inference also needs memory for activations, KV cache, and framework overhead, a safer estimate is smaller than 7B for fp16, or around 7B if using quantization such as 4-bit.
