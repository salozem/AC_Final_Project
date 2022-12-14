# RouteWiseApp
*Final project of the Algorithmic Complexity course.*

##  Anadonda installation

The recommendation is to install miniconda by downloading from
[here](https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe)
and install with default options

If you already have Anaconda installed, or prefer to use Anaconda (larger version)
download from
[here](https://repo.anaconda.com/archive/Anaconda3-2021.05-Windows-x86_64.exe) and
install with default options.

## Create a virtual environment

We create virtual environment to host the flask dependencies. If you use anaconda
you can use the graphical explorer. Here are the steps to
install using command line:

First we open `Anaconda Prompt` or `Anaconda Prompt (miniconda3)` and we execute
the following commands:

```shell
conda update --all
conda create -n comple
conda activate comple
conda update --all
conda install pip
python -m pip install -U pip
python -m pip install Flask
```

Then with our favorite python editor or IDE we create a file called `hello.py` and write the following program: `hello.py`.
`hello.py` and write the following program:

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def hello_world():
    return "<p>Hello, World!</p>"
```

We save the file in a folder of our choice and then, from the previously opened command line, we go to that folder using the command
previously opened command line, we go to that folder using the command
cd`, for example `cd "c:\UsersAkiraToriyama\My Documents"`, if your folder
is on a different disk, first enter the disk name and then the command `cd`, e.g. `d:`d:`.
cd, for example `d:` and then `cd d:\test\test2\tf`.

Finally put the following command:

```shell
set FLASK_APP=hello.py
python -m flask run
```

## Updated Setup

The [venv](https://docs.python.org/3/library/venv.html) module supports the creation of lightweight "virtual environments", each with its own independent set of Python packages installed in its site directories. Virtual environments are recommended for software development projects that are usually derived from a single Python script, and Python provides multiple ways to create and use a virtual environment.

To use venv on your terminal run the following commands

```shell
py -m venv env
```
### Activate venv
```shell
.\env\Scripts\activate
```

### See the list of packages installed in the virtual environment
```shell
pip list
```

### Download the necessary dependencies

```shell
py -m pip install --upgrade pip
pip install Flask
pip install perlin-noise  
```

### Setup to run a web application using Flask and Python3

```shell
cd "Your project path"
set FLASK_APP=tfapp
set FLASK_DEBUG=1

flask run
```

Command to change run port
```shell
python -m flask run -p 5000
```

Now, you will get a URL with a local IP and a port, for example
`http://127.0.0.1:5000`, copy and paste that URL into your favorite browser.

## Important Note

For now you can place your algorithm, as explained in class, in the function
peru1 function of algorithm.py. You must unpack the d.json.zip file directly into the static/data folder and run the application in the normal way, but with
the static/data folder and run the application as normal, but with:

```shell
set FLASK_APP=tfapp.py
python -m flask run
```
