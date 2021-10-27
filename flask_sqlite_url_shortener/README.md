# Url Shortener Version 0.1 alpha
## Develop initialization

```bash
virtualenv .venv
. .venv/bin/activate
pip3 install -r requirements.txt
python3 init_db.py
export FLASK_ENV=development
export FLASK_APP=app
flask run
```
