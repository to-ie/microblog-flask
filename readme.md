# About 
A microblog built on Python Flask based on the tutorial `https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world`

# Notes
Activate the python environment:

`source venv/bin/activate`

set the flask app as a variable to import it:

`export FLASK_APP=microblog.py`

# db migration

create the migration repository for microblog:

`flask db init`
(you probably only need to do this once)

Generates automatic migrations 

`flask db migrate` 
ie: `flask db migrate -m "users table"`

To apply the changes to the database:

`flask db upgrade`

# db erase
```
>>> users = User.query.all()
>>> for u in users:
...     db.session.delete(u)
...
>>> posts = Post.query.all()
>>> for p in posts:
...     db.session.delete(p)
...
>>> db.session.commit()
```

# Run locally
to run the application:

`flask run`

# Activate the python environment:

`source venv/bin/activate`
