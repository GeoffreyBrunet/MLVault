**MOC**:: [[3. ML MOC]]
**Tags**:: #ml #experiment

## Use with Hugging Face Diffuser
### Usefull links
- Model: [https://huggingface.co/CompVis/stable-diffusion-v1-4](https://huggingface.co/CompVis/stable-diffusion-v1-4)
- Documentation: [https://huggingface.co/blog/stable_diffusion](https://huggingface.co/blog/stable_diffusion)
- Use mps (on Apple Silicon): [https://huggingface.co/docs/diffusers/optimization/mps](https://huggingface.co/docs/diffusers/optimization/mps)
### Installation
```shell
conda create --name stablediff
```

```shell
conda activate stablediff
```

```shell
conda install -c conda-forge scipy ffty diffusers
```

```shell
conda install -c pytorch-nightly pytorch
```

```shell
conda install -c huggingface transformers
```

### Script
```shell
python script.py
```
