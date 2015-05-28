# PyTexas Website

## Setting up for development.

Requirements:

- python3
- pip3
- git
- bower
- postgres db

**Ubuntu Requirements:**

```
sudo apt-get install libpq-dev python3-dev python3-pip python3-setuptools libtiff5-dev libjpeg8-dev zlib1g-dev libfreetype6-dev liblcms2-dev libwebp-dev tcl8.6-dev tk8.6-dev python3-tk nodejs npm
sudo npm install -g bower

#db
sudo apt-get install postgresql postgresql-contrib
```

**Site Installation**


```
git clone git@github.com:pytexas/PyTexasWeb.git
git clone git@github.com:pizzapanther/TwoSpaces.git
cd PyTexasWeb/backend/
ln -s ../../TwoSpaces/twospaces/
cd ..
pip3 install -r requirements.txt
cd frontend
bower install
cd ../backend/
cp pytx/settings/local.py.example pytx/settings/local.py
# adjust local.py for your your dev db
./manage.py migrate
./manage.py runserver
```
