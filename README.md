# django-todo-fail
Demonstrates fail for django-todo on heroku.
Reason: setup.py requires django to be installed!

```bash
git clone https://github.com/deniz195/django-todo-fail.git
cd django-todo-fail
heroku create
git push heroku master
```

The build will fail with 

```bash
remote:              File "/tmp/pip-install-vswzjmhl/django-todo/setup.py", line 8, in <module>
remote:                import todo
remote:              File "/tmp/pip-install-vswzjmhl/django-todo/todo/__init__.py", line 12, in <module>
remote:                from . import check
remote:              File "/tmp/pip-install-vswzjmhl/django-todo/todo/check.py", line 1, in <module>
remote:                from django.core.checks import Error, register
remote:            ModuleNotFoundError: No module named 'django'
remote:            ----------------------------------------
remote:        ERROR: Command errored out with exit status 1: python setup.py egg_info Check the logs for full command output.
remote:  !     Push rejected, failed to compile Python app.
```



