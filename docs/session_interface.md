# Session Interface

To use MongoEngine as your session store simple configure the session interface:

```python
from pboot_mongoengine import MongoEngine, MongoEngineSessionInterface

app = Pboot(__name__)
db = MongoEngine(app)
app.session_interface = MongoEngineSessionInterface(db)
```
