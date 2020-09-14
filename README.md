# Set up User On-boarding Using [Dj-Rest-Auth](https://github.com/jazzband/dj-rest-auth) and [Django-All-Auth](https://github.com/pennersr/django-allauth)
A Django web application to search YouTube API. The web application has a search box where user can input search text and a search button to click afterwards to initiate the search. When the button is clicked and the search query is submitted then it leads the user to a page displaying the results of the search.

## How to Set up
For this repository code to work you will need the following tools/softwares installed __Note__: the __*__ indicates the tool/software is required!.
- *Python 3.6+ (Download [here](https://www.python.org/downloads/), instructions [here](https://realpython.com/installing-python/))
- *pip (Set up instructions [here](https://www.liquidweb.com/kb/install-pip-windows/) or [here](https://packaging.python.org/tutorials/installing-packages/#ensure-you-can-run-pip-from-the-command-line))
- Git (Download [here](https://git-scm.com/downloads))
- virtualenv (Set up instructions [here](https://packaging.python.org/tutorials/installing-packages/#creating-virtual-environments))

### Set up steps
1. Open your CLI (Terminal for linux users and Command prompt for windows users)
2. Navigate to your __workspace dir__ using the `cd` command.
3. If you have Git installed simply type the following commands (for both windows and linux users)
```
git clone https://github.com/Semicolon-Tech/django-rest-user-onboarding
cd django-rest-user-onboarding
```

For those that don't have git pre-installed simply click the code button above and click __Download ZIP__. Once the Zip file download is complete, extract the contents to the __workspace dir__. You should rename the directory named _django-rest-user-onboarding-master_ which you should rename to _django-rest-user-onboarding_.

4. This step is optional but __advised__. Set up your _virtualenv_ and __activate__ it by running the following commands
    - #### Windows Users
    ```
    virtualenv venv
    venv\Scripts\activate
    ```

    - #### Linux Users
    ```
    virtualenv venv
    source venv/bin/activate
    ```

Once that is done your next terminal prompt will be prefixed with this __(venv)__. For example,
```
C:\Users\christian\Desktop\youtube-api-search>
```
will become 
```
(venv) C:\Users\christian\Desktop\youtube-api-search>
```

By the way, the name _venv_ can be changed to a different word/name but we will be using venv in this setup instructions.

5. Upgrade your pip by typing the following command
```
python -m pip install pip --upgrade
```

6. Install all python modules in requirements.txt file by typing the following file
```
pip install -r requirements.txt
```

7. Set up the models and database (using SQLite locally)
```
python manage.py migrate
```

8. Create super user credentials
```
python manage.py createsuperuser
```

Fill the required fields when the prompt comes up.

9. Once all packages have been successfully installed run the following command
```
python manage.py runserver
```
it will output a url looking like this `http://127.0.0.1:8000`, visit the url to interact with the application

__Note__: you can find all the API endpoints in the _urls.py_ files. You can also visit `http://127.0.0.1:8000/admin` to see the admin dashboard.


## References
1. [Python 3 Installation & Setup Guide](https://realpython.com/installing-python/)
2. [How to Install PIP on Windows](https://www.liquidweb.com/kb/install-pip-windows/)
3. [Installing Packages (in python)](https://packaging.python.org/tutorials/installing-packages/)