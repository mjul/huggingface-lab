# Huggingface Lab
Taking some Huggingface datasets and transformers for a tour.

## Models
* The Mistral AI 7B base model, see https://huggingface.co/mistralai/Mistral-7B-v0.1
* The Llama2 models from Meta, see https://huggingface.co/meta-llama

## Installation

This repo uses Python 3.11, PyTorch 2.1.0, Huggingface Transformers 4.34 or newer, and JupyterLab notebooks.

We use the transformers with PyTorch. If you are using Conda, install it like this:

    conda install -c pytorch -c nvidia pytorch pytorch-cuda

At the time of writing, the Mistral AI Base Model requires Transformers 4.34, which is not available for
Conda on the main and `huggingface` channels, but only on `conda-forge`. You can install it like this:

    conda install -c conda-forge 'transformers=4.34.0' accelerate=0.23.0 safetensors

We install the optional `transformers` dependency `accelerate` to speed up running on GPUs as it allows the model to be
mapped to CPU and GPU as memory permits. It in turn, requires `safetensors`.

## License
MIT License. See the [LICENSE](LICENSE) file for details.
