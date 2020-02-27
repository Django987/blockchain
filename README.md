According Blog:
https://hackernoon.com/learn-blockchains-by-building-one-117428612f46

1. check if python installed 
* Windows 10: open CMD > 
```shell
python -V
```

*not installed > [Download Windows x86-64 executable installer] [0]

## Pitfalls

### Dependency in Flask 
[Source][1]

pip install --upgrade Flask

resolves > AttributeError: 'Request' object has no attribute 'is_xhr'

---

### NoneType is not iterable when checking Post-Body Parameters 
[Source][2]

```python
    def new_transaction():
        values = request.get_json(force=True)
```

instead of 

```python
    def new_transaction():
        values = request.get_json()
```


## Miscellaneous

For Debugging a Flask App set an environment variable (using CMD)  
[Source][3]

> set FLASK_ENV=development

[0]: https://www.python.org/downloads/windows/
[1]: https://stackoverflow.com/questions/60131900/weird-is-xhr-error-when-deploying-flask-app-to-heroku
[2]: https://github.com/dvf/blockchain/issues/75
[3]: https://stackoverflow.com/questions/17309889/how-to-debug-a-flask-app

