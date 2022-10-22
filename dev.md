# Programming environment for python devs

## _Basic instructions for developers environment base_

[install gitbash](#install-git-bash)\
[install windows terminal](#install-windows-terminal)\
[install python and anaconda](#install-python-using-anaconda-distribution)\
[setup jupyter notebook](#run-jupyter-notebook-on-browser)\
[colab local server](#colab-local-server)

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
