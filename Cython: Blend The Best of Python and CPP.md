Python Syntax looks like this
```
def fib(n):
    a,b = 1,1
    for i in range(n):
        a,b = a+b,a
    return a
```
C++ Syntax looks like this
```
int fib(int n):
{
    int temp, i, a, b;
    a = b = 1;
    for(i=0; i<n, i++)
    {
    tmp = a;
    a += b;
    b = tmp;
    }
}
```

Python Syntax looks like this
Cython version has to convert python object to c++ objects, so there is additional overhead
```
def fib(int n):
    cdef int i, a, b
    a,b = 1,1
    for i in range(n):
        a,b = a+b,a
    return a
```

If you write the extension module in C manually you would be able to get 25x faster

What is Cython?
- Cython is Python-like language that
- Improves Python Performance
- Wraps External Libraries

Cython command
- Generates optimized c++ source file from Cython source file
- Built in support for Numpy
- Integrates with IPython

**Website**: www.cython.org

##### Cython Workflow
fib.pyx (Python) -> fib.c (C++) -> fib.so (C Compiled)

### Compiling with distutils
```
setup(name="fib", ext_modules=cythonize("fib.pyx"))
python setup_fib.py build_ext --inplace
```

### pyximport
pyximport: Import Cython source file as if it is a pure python module
Detects changes in cython file, recompiles if necessary, loads cached module if not > Great for interactive dev

```python
import pyximport
pyximport.install()
from fib import fib
print(fib(10))
```

### Using with Jupyter Notebook


```python
%load_ext cythonmagic


%% cython
#This cells is treated as cython code>
#It will compile and load everything automatically
```

### def vs cdef vs cpdef
- def functions can be called from python
  - Serves as minimum wrapper
- cdef functions can be called from cython and C
  - This will be faster than just using def function
- cpdef : allow function to call from Python or Cython.
    Data types need to be compatible with both C and Python
```cython
cdef class Particle(object):
    cdef float a
    cdef str b
```


### Using Hello World

```python
from distutils.core import setup
from Cython.Build import cythonize

setup(name="cython_hello_world", ext_modules=cythonize("cython_hello_world.pyx"))
```

### Debugging
Using standard GDB compiler for debugging

### Tips and Tricks
- Always type loop related variables to make interpretation easy
