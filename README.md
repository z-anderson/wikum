# wikum

## Local install

1. git clone https://github.com/amyxzhang/wikum.git
2. `cd wikum/wikum`
2. Install pip and [virtualenv](https://virtualenv.pypa.io/en/latest/)
3. `virtualenv wikum`
3. `mkdir /opt/wikum`
3. `echo "true" > /opt/wikum/debug`
4. `echo "prod" > /opt/wikum/env`
5. `touch private.py`
6. `vim private.py`
7. Inside private.py, paste this to connect to the remote database, then `:wq`: 
	```
	MYSQL_PROD = {
	    'NAME' : 'wikum',
	    'USER' : (ask me),
	    'PASSWORD' : (ask me),
	    'HOST' : 'mysql.csail.mit.edu',  
	}
	```
	
8. `wikum/bin/activate`
9. `pip install -r requirements.txt`
9. `python manage.py runserver`
