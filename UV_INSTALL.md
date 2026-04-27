Install with UV using the following commands:

```bash
# Step 1: install everything but pybullet-svl and pytorch3d with
uv sync

# Step 2: downgrade setuptools so pybullet-svl's setup.py can find pkg_resources
# (pybullet-svl uses pkg_resources which was removed in setuptools>=70)
uv pip install "setuptools<70"
uv pip install --no-build-isolation "pybullet-svl==3.1.6.4"

# Step 3: build pytorch3d with the populated venv (needs torch available at build time)
uv pip install --no-build-isolation "pytorch3d @ git+https://github.com/facebookresearch/pytorch3d.git"
```
