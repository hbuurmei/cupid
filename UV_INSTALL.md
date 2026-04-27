Install with UV using the following commands:

```bash
# Step 1: install everything but pybullet-svl and pytorch3d with
uv sync

# Step 2: build pybullet-svl and pytorch3d with the populated venv
uv pip install --no-build-isolation "pybullet-svl==3.1.6.4"
uv pip install --no-build-isolation "pytorch3d @ git+https://github.com/facebookresearch/pytorch3d.git"
```
