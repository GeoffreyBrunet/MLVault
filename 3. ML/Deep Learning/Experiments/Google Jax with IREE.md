**MOC**:: [[3.2. DL MOC]]
**Tags**:: #ml #experiment 

# Setup
1. Create virtual environnement:
```shell
conda create -n jax-iree
```
2. Activate virtual environnement:
```
conda activate jax-iree
```
3. Install IREE
```shell
python -m pip install iree-compiler iree-runtime --find-links https://iree-org.github.io/iree/pip-release-links.html
```
4. Install Jax (python API) and Jaxlib (C/C++ library):
```shell
pip install --upgrade jax jaxlib
```
5. Run script:
```shell
JAX_ENABLE_MLIR=1 JAX_PLATFORMS=iree python main.py
```
