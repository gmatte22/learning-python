## Python Virtual Environment

More details here [https://docs.python.org/3/tutorial/venv.html](https://docs.python.org/3/tutorial/venv.html) regarding python virtual environments.  
> tl;dr: Python virtual environments are separate and independent python shells that don't mess with your system or other projects. They are linked back to your system Python executables, but this shell allows you to install whatever packages you want and they are stored separately. Python venvs are a best practice, and often the only way to maintain sanity.

Let's create a virtual environment called "workspace" that we can use. (You can call it whatever you want. Ideally it will be called something specific to whatever project you're working on.) In this environment we can install whatever python libraries and packages we want and it won't interfere with our base installations above. 

First we'll create a subdirectory for this and any other python virtual environments that we'll want down the road. You can put this wherever you want. I generally create it here:

`mkdir -p ~/python_envs`

Next we'll use the "venv" command to create our "workspace" environment under this location:

```
cd ~/Desktop/python_envs
python3 -m venv workspace
```

Then whenever you want to use this environment, you activate it by typing:

`source ~/workspace/bin/activate`

Notice this will add a indicator to your prompt letting you know what your venv is:

```
(workspace) ~$  python --version 
Python 3.9.6
```

When you are done with that venv you can either close your terminal session or just type:

`deactivate workspace`
