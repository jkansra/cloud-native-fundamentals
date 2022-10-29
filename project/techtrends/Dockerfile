# use the python:3.8 base image
FROM python:3.8

# copy files from the host to the container filesystem. 
# For example, all the files in the current directory
# to the  `/app` directory in the container
COPY . /app
#  defines the working directory within the container
WORKDIR /app

# import dependencies using `pip install -r requirements.txt` and the database is initialized with the pre-defined posts in the init_db.py file
RUN pip install -r project/techtrends/requirements.txt
RUN python init_db.py

# expose the port 3111
EXPOSE 3111

# start the container by invoking the app.py file
CMD [ "python", "app.py" ]
