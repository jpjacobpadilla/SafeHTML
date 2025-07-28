## SafeHTML

A simple package that uses the new template string syntax in (PEP 750) in Python `3.14.0b1` or higher.

```python
from safehtml import html

name = "Jacob <script>alert('xss')</script>"
print(html(t"<p>Hello {name}</p>"))
```

Output:
```plaintext
<p>Hello Jacob &lt;script&gt;alert(&#x27;xss&#x27;)&lt;/script&gt;</p>
```

## Install

```bash
uv init --python 3.14.0rc1
```

```bash
uv add safehtml
```