pip install --upgrade Flask

resolves > AttributeError: 'Request' object has no attribute 'is_xhr'

https://stackoverflow.com/questions/60131900/weird-is-xhr-error-when-deploying-flask-app-to-heroku

Debug Flask App
CMD: set FLASK_ENV=development

def new_transaction():
    values = request.get_json(force=True)

instead of 

def new_transaction():
    values = request.get_json()