1. creating a virtual environment.

	python3 -m venv newenv--without-pip

	source newenv/bin/activate

2. next installing the heroku command line tools with the following command:
curl https://cli-assets.heroku.com/install-ubuntu.sh | sh


3. checking the installation with the command:
heroku —-version

4. logging into heroku using the command:
heroku login -i
and then enter your email and password when asked

5. creating a procfile with the command
	touch Procfile
and put the following in the Procfile
	web gunicorn run:app

6.Then create a requirements file with this command(did it only once):
pip freeze > requirements.txt
and changing versions which were giving errors earlier 

7. Next, initialize a git repository with the following commands:
	git init
	git add .

8. configure the email and user name, you can use these commands:
git config --global user.email email@example.com
git config --global user.name "my name"

9. make a commit with this command:
git commit -m "first commit"

10. create a uniquely named heroku app. Use this command:
heroku create my-app-name

11. check that heroku added a remote repository with this command:
git remote -v

12. push the app to Heroku:
git push heroku master