# EMIT_School

## Set up PyCBC in a new conda environment

1. Create a new conda environment. Please follow the steps discussed here: https://code.visualstudio.com/docs/python/environments . I am using Python 3.9.16 Interpreter.

2. Install pycbc and its dependencies using pip: pip install pycbc

3. I just noticed that there is an error while initializing the EmceePT sampler in cell 14. The error is as follows:

"AttributeError: module 'numpy' has no attribute 'float'.`np.float` was a deprecated alias for the builtin `float`. To avoid this error in existing code, use `float` by itself. Doing this will not modify any behavior and is safe. If you specifically wanted the numpy scalar type, use `np.float64` here."

I was using the latest version of numpy 1.25.1 in my conda environment. By downgrading its version to 1.23.0, the error vanished so if anyone is facing similar error please downgrade numpy version. To downgrade, use the following command: pip install numpy==1.23.0 
