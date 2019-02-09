```bash
mypy minimal_mypy_import/
minimal_mypy_import/__init__.py:3: error: Name 'a_value' is not defined
```

If we switch `a/__init__.py` from:

```python
from .file import *

__all__ = file.__all__
```

To:

```python
from .file import *

__all__ = ["a_value"]
```

MyPy can check this OK.
