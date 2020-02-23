According Blog:
https://hackernoon.com/learn-blockchains-by-building-one-117428612f46

## Pitfalls

### Dependency in Flask

pip install --upgrade Flask

resolves > AttributeError: 'Request' object has no attribute 'is_xhr'

https://stackoverflow.com/questions/60131900/weird-is-xhr-error-when-deploying-flask-app-to-heroku

---
### NoneType is not iterable when checking Post-Body Parameters

https://github.com/dvf/blockchain/issues/75


```python
    def new_transaction():
        values = request.get_json(force=True)
```

instead of 

```python
    def new_transaction():
        values = request.get_json()
```

---

#### Miscellaneous

Debug Flask App
CMD: set FLASK_ENV=development

