# About

Blender has a Python scripting API, but it is limited to an interpreter launched within Blender. This Jupyter kernel starts a Blender instance with an async kernel running inside of it. This means that you can script from [hydrogen](https://github.com/nteract/hydrogen) or a [Notebook](https://jupyter.org/) while still using the Blender UI.

# Installation

Find your `DATA_DIR` with `jupyter --data-dir`. Your `KERNEL_DIR` is `DATA_DIR/kernels/`

1. `git clone https://github.com/cameronfr/BlenderKernel`
1. In `kernel.json`, replace `KERNEL_DIR` with your `KERNEL_DIR`
2. In `KernelFile.py`, replace `pythonPath` with a python site-packages path
3. In `KernelFile.py`, replace `blenderPath` with a path to your Blender executable
2. `mv BlenderKernel KERNEL_DIR/blender`

Use `jupyter kernelspec list` to make sure the kernel is listed, then launch the kernel as you would any other. 

To test on the default cube scene, 
- run `import bpy`  
- the Cube should move when you run `bpy.data.objects["Cube"].location[0] += 0.5` .
