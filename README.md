# O'Reilly Live Course: Open Source Reasoning Language Models

Repository for the course with all material. 

## Presentation
The [slides](<2026-09-28-Reasoning.pdf>) contain additional
background and theroretical information.

## Python setup 

### uv
If possible, work with [uv](https://astral.sh/uv/). Clone the repository and run `uv sync`.
However, there are some challenges:
* Most of the notebooks work with `pyproject.toml`.
* Currently, the lastest `transformers` is not compatible with both `SGLang` and `unsloth`. I recommend using different kernels for that.
* Some notebooks are specifically suited for MacOS using the `mlx-lm` package. It is only useful to install that with a Mac.

### anaconda

Create an venv or conda environment and install the following packages for the normal notebooks:
* accelerate
* causal-conv1d
* datasets
* flash-linear-attention
* ipython
* jupyter
* kernels
* liger-kernel
* math-verify
* openai
* openrouter
* peft
* torch
* triton
* trl

For `unsloth` you just need to install `unsloth` and `vllm`.

For `SGLang`, you just have to install `sglang` or use `uvx run sglang`.

For MacOS notebooks, the following packages are recommended:
* jupyter
* mlx-lm
* mlx-vlm
* mlx-optiq
* openai
* openrouter


I have not provided a `requirements.txt` as dependencies tend to get outdated faster that I can update.

## runpod

You can also use runpod. `uv` is already preinstalled there. Of course, the MacOS notebooks won't work there.

## Notebooks

You can either try to run the notebooks directly
or try to follow how I run them and use it as a 
documentation (or run it later).


### Running different models with GPUs or Macs directly in the notebook
* [11-qwen3.5-9b-cuda.ipynb: Small Qwen3.5 model on CUDA](11-qwen3.5-9b-cuda.ipynb)
* [12-qwen3.5-9b-mlx.ipynb: Same model for Mac](12-qwen3.5-9b-mlx.ipynb)

## Running models with platform-specific external server software
* [21-gemma-4-12b-qat-cuda-sglang.ipynb: `SGLang` as an external server for CUDA](21-gemma-4-12b-qat-cuda-sglang.ipynb)
* [22-gemma-4-12b-qat-mlx-serve.ipynb: `optiq` as an external server on Macs](22-gemma-4-12b-qat-mlx-serve.ipynb)

## Running models platform-independently with `llama.cpp`
* [23-qwen3.8-27b-llamacpp.ipynb: `llama.cpp` as a universal solution, also for bigger models](23-qwen3.8-27b-llamacpp.ipynb)

## Testing different models with *OpenRouter*
* [31-openrouter.ipynb: OpenRouter allows easy testing of models](31-openrouter.ipynb)


### Finetuning with GRPO
* [41-finetune-numinamath-grpo-trl-qwen.ipynb: Finetune a small Qwen model with Hugging Face trainer](41-finetune-numinamath-grpo-trl-qwen.ipynb)
* [41-finetune-numinamath-grpo-trl-qwen-complete.ipynb: same as above, but with output](41-finetune-numinamath-grpo-trl-qwen-complete.ipynb)
* [42-unsloth-qwen3-4-base.ipynb: Train a larger Qwen3 base model with `unsloth`](42-unsloth-qwen3-4-base.ipynb)
* [42-unsloth-qwen3-4-base-complete.ipynb: same as above, but with output](42-unsloth-qwen3-4-base-complete.ipynb)
