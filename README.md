# Crypto

Bitcoin trading application

[![CircleCI](https://circleci.com/gh/nikoren/crypto/tree/master.svg?style=svg)](https://circleci.com/gh/nikoren/crypto/tree/master)
  
### Configuration `config.py`
- Main db is Postgresql , sqlite is not fully supports all the features but can be used for basic setup

```python
    SQLALCHEMY_DATABASE_URI = os.environ.get('DEV_DATABASE_URL') or \
                               'sqlite:///' + os.path.join(basedir, 'data-dev.sqlite')
    SQLALCHEMY_DATABASE_URI = 'postgresql://localhost/{}'.format(Config.PROJECT_NAME.lower())
```

### Getting started

```bash
# clone this project
pip install -r requirements.txt
python manage.py shell 
db.create_all()
╰─$ python manage.py runserver
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
 * Restarting with stat
 * Debugger is active!

```

