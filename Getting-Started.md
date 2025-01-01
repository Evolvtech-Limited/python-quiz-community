## Project Setup for Developers
We are using [gulp](https://gulpjs.com/) which allows having complete automation for build flow. In case if you don't know Gulp then it's easy to use it. Gulp is a toolkit for automating painful or time-consuming tasks in the development workflow, so you can stop messing around while building any project. You can read it more about it [here](https://gulpjs.com/).

### Prerequisites:
Please follow the below steps to install and setup all prerequisites:

- <b>Nodejs<b/> <br />
Make sure to have [Node.js](https://nodejs.org/) installed & running on your computer. If you already have installed Node on your computer, you can skip this step if your existing node version is greater than 18. We suggest you to use LTS version of Node.js.

- Yarn <br />
Make sure to have the [Yarn](https://classic.yarnpkg.com/en/) installed & running on your computer. If you already have installed Yarn on your computer, you can skip this step. We suggest you use Yarn instead of NPM.

- Gulp <br/>
Make sure to have the [Gulp](https://gulpjs.com/) installed & running on your computer. If you already have installed gulp on run command ```npm install -g gulp``` from your terminal.

- Git <br/>
Make sure to have [Git](https://git-scm.com/) installed globally & running on your computer. If you already have installed git on your computer, you can skip this step.

- Python
Make sure to have the [Python](https://www.python.org/downloads/) installed & running in your computer. If you already have installed Python on your computer, you can skip this step. Please use Python version 3 or if you are using python version 2 then make sure to run all the below commands with python insted of python3.

#### For windows
- Download python from windows store
- Select the Python's version to download.
- Click on the Install Now
- Installation in Process

#### For Linux
- sudo apt update
- sudo apt install python3

#### Check Pip version
    ```bash
    py -m pip --version
    upgread pip
    py -m pip install --upgrade pip

#### Virtualenv
Make sure to have the ```virtualenv``` installed globally & running on your computer. If you already have installed on your computer, you can skip this step.

Virtualenv installation command for linux & mac os <br/>
```python3 -m pip install --user virtualenv``` <br />
Virtualenv installation command for Windows  <br />
```py -m pip install --user virtualenv```

After you finished with the above steps, you can run the following commands into the terminal/command prompt from the root directory ( python-quiz-community/admin ) of the project to run the project locally or build for production use:

| Command                                    | Description                                                                  |
|--------------------------------------------|------------------------------------------------------------------------------|
| `yarn install`                             | This would install all the required dependencies in the node_modules folder. |
| `gulp`                                     | It will generate the static folder.                                          |
| `python3 -m pip install --user virtualenv` | Create Virtual Environment on linux & mac OS                                 |
| `py -m pip install --user virtualenv`      | Create Virtual Environment on Windows OS                                     |
| `source environment_name/bin/activate`     | Activate Environment on Linux & mac OS                                       |
| `environment_name/Scripts/activate`        | Activate Environment on Windows OS                                           |
| `python -m pip install Django`             | Install Django on linux & mac OS                                             |
| `py -m pip install Django`                 | Install Django on Windows OS                                                 |

<h3>Note:</h3> Depending on your installation, you may need to use either pip3 or pip and for python you may need to use either python3 or python.

- After you finished with the above steps, you can run the following commands into the terminal / command prompt from the root directory of the project to run the project locally:

- Install few libraries
    ```bash
    pip install django-allauth
    pip install django-embed-video
    pip install django-crispy-forms
    pip install django-multiselectfield
    pip install crispy-bootstrap5
    pip install Pillow

### Database Connectivity
Goto `settings.py` of main directory and update below settings. <br />

    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.#databaseservername#',
            'NAME': 'Your Database Name',
            'USER' : 'Database User Name',
            'PASSWORD' : 'Your Password',
            'HOST' : 'Write down Host',
            'PORT' : 'Write down port',
        }
    }

#### Run below command for database migration
    ```bash
    python manage.py migrate

#### To create a superuser run the below command
    ```bash
    python manage.py createsuperuser

    enter username Your Username
    enter your Email Address
    enter your Password
    enter your Password again

#### To load static files
    Go to Velzon/settings.py and add following command:-
    STATIC_URL = '/static/'
    STATICFILES_DIRS = [os.path.join(BASE_DIR,'static')]
    python manage.py collectstatic

    SMTP CONFIGURATION
    EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
    EMAIL_HOST = 'smtp.mailtrap.io'
    EMAIL_PORT = 2525
    EMAIL_USE_TLS = True
    EMAIL_HOST_USER = 'YOUR EMAIL ADDRESS'
    EMAIL_HOST_PASSWORD = 'YOUR HOST Password'
    DEFAULT_FROM_EMAIL = 'YOUR EMAIL ADDRESS'

#### Run below command for run your project
    python manage.py runserver

<h3>Note: </h3> We suggest you do not change any scss files from the src/scss/custom folders because getting new updates will break your SCSS changes if any you have made. We strongly suggest you create a new custom.scss file and use that instead of overwriting any theme's custom scss files.