# Programming environment for python devs

## _Basic instructions for developers environment base_

[install gitbash](#install-git-bash)\
[install windows terminal](#install-windows-terminal)\
[install python and anaconda](#install-python-using-anaconda-distribution)\
[setup jupyter notebook](#run-jupyter-notebook-on-browser)\
[colab local server](#colab-local-server)
[for linux](#linux-environment)

## Install git bash

- download gitbash from [official website](https://git-scm.com/downloads)
- install git bash keeping all the settings to default
- click next next

## Install windows terminal

1. download windows terminal from [MS store](https://www.microsoft.com/store/apps/9n0dx20hk701)
> to setup git bash in windows terminal follow the steps below
3. open windows terminal and go to settings
4. add new profile
5. click new empty profile
6. change the name to **gitbash**
7. replace the command line with this location
   `C:\Program Files\Git\bin\bash.exe`
8. choose custom icon or use default icon from this location
   `C:\Program Files\Git\mingw64\share\git\git-for-windows.ico`
9. go startup tab and choose gitbash as default profile

## Install python using anaconda distribution

- download conda from [official website](https://www.anaconda.com/products/distribution)
- click next next untill `advance installation option`
- check both of the options

## Run jupyter notebook on browser

> open terminal and run the commands below

```sh
jupyter notebook
```
_**this will create notebook file on default browser**_

## Colab local server

> if you are using google colab instead of jupyter notebook you can also use this local compiler for colab
1. copy paste the commands below in terminal
```sh
pip install jupyter_http_over_ws
```

```sh
jupyter notebook --NotebookApp.allow_origin="https://colab.research.google.com" --port=8888 --NotebookApp.port_retries=0
```
2. now the token URL (_local host one_) generated in terminal: [reference image](https://robotwealth.com/wp-content/uploads/2020/11/jupyter-local.png)
3. In Colab, click the `Connect` button and select `Connect to local runtime`. Enter the token URL you just copied and click `Connect`: [reference image](https://robotwealth.com/wp-content/uploads/2020/11/colab-connect-local.png)\
_**Now code will run lot faster**_

## linux-environment
## install python & jupyter notebook

1. setting up python - `once`

```sh
sudo apt update
```

```sh
sudo apt install python3-pip python3-dev
```

2. installing python & jupyter - `once`

```sh
sudo -H pip3 install --upgrade pip
```

```sh
sudo -H pip3 install virtualenv
```

3. create a python project directory - `once`
```sh
mkdir ~/python_project
```

4. move inside of that directory - `once`
```sh
cd ~/python_project
```

5. creating virtual environemnt - `once`

```sh
virtualenv python_virtual_env
```

```sh
source python_virtual_env/bin/activate
```

>now your terminal prefix should look similar to this
 `(python_virtual_env) example@host:~/python_project_dir$`

6. installing jupyter - `once`

```sh
pip install jupyter
```

7. running jupyter notebook

```sh
jupyter notebook
```

> below steps are optional who want to use jupyter as a runtime for google colab

8. enable http extension - `once`

```sh
pip install jupyter_http_over_ws
```

```sh
jupyter serverextension enable --py jupyter_http_over_ws
```

9. run jupyter as local runtime
- go to your python environment directory we created earlier
- run command below
```sh
jupyter notebook \
  --NotebookApp.allow_origin='https://colab.research.google.com' \
  --port=8888 \
  --NotebookApp.port_retries=0
```


