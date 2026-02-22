# O'Reilly Live Course: Open Source Reasoning Language Models

Repository for the course with all material. 

## Presentation
The [slides](<2026-02-24-Reasoning.pdf>) contain additional
background and theroretical information.

## Python setup 

### uv
If possible, work with [uv](https://astral.sh/uv/). Clone the repository and run `uv sync`.
However, there are some challenges:
* Most of the notebooks work with `pyproject.toml`.
* Currently, the lastest `transformers` is not compatible with both `vllm` and `unsloth`. I recommend using a different kernel for that.
* Some notebooks are specifically suited for MacOS using the `mlx-lm` package. It is only useful to install that with a Mac.

### anaconda

Create an venv or conda environment and install the following packages for the normal notebooks:
* accelerate
* datasets
* flash-attn
* ipython
* jupyter
* kernels
* liger-kernel
* peft
* transformers
* triton
* trl

`flash-attn` should be installed with the option `--no-build-isolation`.

For `unsloth` and `vllm`, you can use:
* datasets
* ipykernel
* jupyter
* transformers
* trl
* unsloth
* vllm

For MacOS notebooks, the following packages are recommended:
* jupyter
* mlx-lm

I have not provided a `requirements.txt` as dependencies tend to get outdated faster that I can update.

## runpod

You can also use runpod. `uv` is already preinstalled there. Of course, the MacOS notebooks won't work there.

## Notebooks

You can either try to run the notebooks directly
or try to follow how I run them and use it as a 
documentation (or run it later).


### Running different models with GPUs
[11-deepseek-distill-qwen3-8.ipynb: Use a distilled DeepSeek model](11-deepseek-distill-qwen3-8.ipynb)
[12-qwen3-8.ipynb: Use a hybrid Qwen3 model with 8B parameters](12-qwen3-8.ipynb)
[13-nanbeige-3.ipynb: Use a new, very small and powerful model](13-nanbeige-3.ipynb)
[14-nanbeige-3-tool.ipynb: Same as before, but with reasoning (e.g. agentic usage)](14-nanbeige-3-tool.ipynb)
[15-mimo-7.ipynb: Use MiMo model from Xiaomi](15-mimo-7.ipynb)
[16-gpt-oss-20.ipynb: Use GPT-OSS from OpenAI with efficient MXFP4 datatype](16-gpt-oss-20.ipynb)
[17-qwen3-0.6.ipynb: Use a small Qwen3 model](17-qwen3-0.6.ipynb)
[21-qwen3-8-awq-vllm.ipynb: Use a quantized model with vLLM for optimized generation](21-qwen3-8-awq-vllm.ipynb)

### Running different models on MacOS
[31-mlx-deepseek-qwen3-8b.ipynb: Run the Qwen3 8B model on MacOS](31-mlx-deepseek-qwen3-8b.ipynb)
[32-mlx-qwen-30-3.ipynb: Run a larger Qwen3 30B model with 3B active parameters on MacOS](32-mlx-qwen-30-3.ipynb)

### Finetuning with GRPO
[41-finetune-numinamath-grpo-trl-qwen.ipynb: Use Hugging Face `trl` to train a model](41-finetune-numinamath-grpo-trl-qwen.ipynb)
[41-finetune-numinamath-grpo-trl-qwen-complete.ipynb: Same as before, but with output](41-finetune-numinamath-grpo-trl-qwen-complete.ipynb)
[42-unsloth-qwen3-4-base.ipynb: Use a combination of `unsloth` and `vllm` to train a model](42-unsloth-qwen3-4-base-complete.ipynb)
[42-unsloth-qwen3-4-base-complete.ipynb: Same as before, but with output](42-unsloth-qwen3-4-base-complete.ipynb)
