# Description
This is a Flask Restful example project ready to deploy on cPanel.

# Auto Deploy to Cpanel
* Change `.cpanel.yml.example` filename to `.cpanel.yml`
* Edit `/home/user/pythonapp` line in `.cpanel.yml` to your username on cPanel
## Example cpanel.yml File
```yml
---
deployment:
  tasks:
    - export DEPLOYPATH=/home/user/pythonapp/
    - /bin/mkdir $DEPLOYPATH
    - /bin/cp app.py $DEPLOYPATH
    - /bin/cp passenger_wsgi.py $DEPLOYPATH
    - /bin/cp requirements.txt $DEPLOYPATH
    - /bin/mkdir $DEPLOYPATH/tmp
    - /bin/touch $DEPLOYPATH/tmp/restart.txt
```

# Source
Todo App Source: [Flask Documentation](https://flask-restful.readthedocs.io/en/latest/quickstart.html#a-minimal-api)
