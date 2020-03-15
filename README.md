# django-uwsgi
## Source
Created from the content on this [page](https://www.caktusgroup.com/blog/2017/03/14/production-ready-dockerfile-your-python-django-app/)

## Usage
1. Update the *requirements.txt* file as necessary
2. Put the *Dockerfile*, *docker-compose.yml*, *requirements.txt*, and *entrypoint.sh* files in the root directory.  Your manage.py file should also be in this location.
3. Update the *Dockerfile* and make sure paths (your codebase) and ports are correct and db information is correct
4. Update the *docker-compose.yml* file if you changed any ports in the previous step or if you need to alter the db connection info
5. Start it up using *docker-compose up --build -d*

## Troubleshooting
If you need to connect to the machine to troubleshoot, try *docker exec -it django-uwsgi_app_1 base*
The container name should be *django-uwsgi_app_1* but you may want to use *docker ps* to confirm.



