How to install Django on Windows
https://docs.djangoproject.com/en/2.0/howto/windows/
open the command prompt and check that the Python version matches the 
version you installed by executing:
>> python --version
//=============================================================================
pip is a package manage for Python. It makes installing and uninstalling Python 
packages (such as Django!) very easy
https://pip.pypa.io/en/latest/installing/
//=============================================================================
virtualenv and virtualenvwrapper provide a dedicated environment for each Django 
project you create. While not mandatory, this is considered a best practice and 
will save you time in the future when you’re ready to deploy your project. 
Simply type:
>> pip install virtualenvwrapper-win
//=============================================================================
You are using pip version 9.0.2, however version 10.0.1 is available.
You should consider upgrading via the 
>> python -m pip install --upgrade pip
command.
//=============================================================================
Then create a virtual environment for your project:
>> mkvirtualenv myproject
C:\Users\aozdemir\Envs is not a directory, creating
//=============================================================================
The virtual environment will be activated automatically and you’ll see 
“(myproject)” next to the command prompt to designate that. If you start a new 
command prompt, you’ll need to activate the environment again using:
>> workon myproject
//=============================================================================
Django can be installed easily using pip within your virtual environment.
In the command prompt, ensure your virtual environment is active, and execute 
the following command:
>> pip install django
//=============================================================================
After the installation has completed, you can verify your Django installation 
by executing 
>> django-admin --version 
in the command prompt.
//=============================================================================
If you are upgrading your installation of Django from a previous version, 
you will need to uninstall the old Django version before installing the new 
version.
//=============================================================================
If you previously installed Django using python setup.py install, uninstalling 
is as simple as deleting the django directory from your Python site-packages. 
To find the directory you need to remove, you can run the following at your 
shell prompt (not the interactive Python prompt):
$ python -c "import django; print(django.__path__)"
['C:\\Users\\aozdemir\\Envs\\myproject\\lib\\site-packages\\django']
//=============================================================================
From the command line, cd into a directory where you’d like to store your code, 
then run the following command:
https://stackoverflow.com/questions/43928517/django-admin-is-not-working-django-1-11-python-3-6
$ workon myproject
$ django-admin startproject mysite .
//=============================================================================
You’ll need to avoid naming projects after built-in Python or Django components. 
In particular, this means you should avoid using names like django (which will 
conflict with Django itself) or test (which conflicts with a built-in Python 
package).
//=============================================================================
The development server¶
Let’s verify your Django project works. Change into the outer mysite directory, 
if you haven’t already, and run the following commands:
$ python manage.py runserver
http://127.0.0.1:8000/
//=============================================================================
