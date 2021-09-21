# Run a python script that has a venv

Provided you keep a clean machine where every single Python project gets its own venv, if you want to run that script via cron or just as an alias or from the CLI:

```
/path/to/your/project/.venv/bin/python /path/to/your/project/script.py
```

This likely won't work if you have a custom $PYTHONPATH set up.

You can also do this via cron or an alias:

```
0,30 * * * * cd /path/to/your/project && .venv/bin/python script.py > /dev/null 2>&1
```

```
alias myscript="/path/to/your/project/.venv/bin/python /path/to/your/project/script.py"
```