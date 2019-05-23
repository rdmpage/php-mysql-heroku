# php-mysql-heroku
PHP app with MySQL

- Create repository in GitHub

- Clone the repository

- ```composer init``` will create basic composer.json file and asks whether you want to add "vendor/" to .gitignore (say ```yes```)

- Create simple index.php file

- Create a Heroku app ```heroku create```
```https://floating-reef-41010.herokuapp.com/```

- Go to dashboard.heroku.com and connect the newly created app to your Github repository.

- Click **Deploy Branch** button.

- Add database as an add-on either via command line ```heroku addons:create cleardb:ignite``` or via dashboard.

- The database URL is visible on Settings tab as one of the Config Vars, and has the form mysql://(user name):(password)@(host)/(database name):

```mysql://bd7aff43608547:7c15ef4f@us-cdbr-iron-east-02.cleardb.net/heroku_e025d395e9cd915?reconnect=true```

- You can connect to your database like this:

```mysql -u bd7aff43608547 -h us-cdbr-iron-east-02.cleardb.net -p heroku_e025d395e9cd915```

You will be prompted for the database password (or you can put it in the command line above after the ```-p```.

- To upload data:

```mysql -u bd7aff43608547 -h us-cdbr-iron-east-02.cleardb.net -p heroku_e025d395e9cd915 < data.sql```






