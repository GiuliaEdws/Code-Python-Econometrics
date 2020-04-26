## Python Management Guide

### Check existing python versions: 

```
which -a python
which -a python3
```

### Uninstall Old Versions of Python, If Needed

Warning: DO NOT uninstall system version of python. Check the guide [here](https://www.ianmaddaus.com/post/manage-multiple-versions-python-mac/#locate-python) for the correct way to uninstall versions that you did yourself.  

### Install Python via Homebrew

* The advantage of using homebrew over anaconda installed-python is that you have more control over what you install. Conda is nothing fancy, you can have the same packages by hand with a combination of `pip` and Homebrew core.  See discussion [here](https://www.slant.co/versus/1592/1674/~conda_vs_homebrew).

* For the numerical applications you will probably want to have the latest versions of your packages at all times. You can use your virtualenvs only when you do web development.

First, check if homebrew is correctly installed by running

```brew doctor
brew doctor
```

Fix issues as given by its warning when needed. 

Then install Python 3:

```
brew install python3
```

Check version and test run:

```
python3 --version
python3
```



After installation, add the new version to bash file, by:

```
echo 'export PATH="/usr/local/sbin:$PATH"' >> ~/.bash_profile
```

And to use Jupyter notebook, install the following from anew:

```
pip3 install ipython
python3 -m pip install jupyter
```

__Note:__ after reinstallation, packages need to be reinstalled. From now on, use `pip3` instead of `pip` to install new packages.