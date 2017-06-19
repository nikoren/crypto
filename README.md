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

git clone git@github.com:nikoren/crypto.git
# make sure you have python3.6 installed
venv_path=/path/to/crypto_venv
python -m venv $venv_path
source  $venv_path/bin/activate
# install dependencies
pip install -r requirements.txt
cd app
ipython
from cryptotrader2 import main
main()
```

