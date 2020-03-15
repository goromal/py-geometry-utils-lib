# python_utilities

Python3 wrappers for the *geometry-utils-lib* package.

## Installation and Usage

Enter the *pylib* directory and build the python bindings with CMake:

```bash
cd pylib/
cmake ..
make
```

To use the modules in this repository, include the following lines at the top of your Python script:

```python
#!/usr/bin/python3
import sys
sys.path.insert(1, '/path/to/pylib')
```
