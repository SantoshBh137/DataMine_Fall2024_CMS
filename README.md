
This github is designed for students of PHYS_323 for fall semester. The notebooks that will be presented here are created by PHD students Andrew Wildridge and Lingqiang He. Please follow the instruction below to connect to Jupyterlab/notebook. 

# Connecting to Jupyter Lab/Notebook
First <br>
```
ssh <user_name>@scholar.rcac.purdue.edu -L <port_number>:localhost:<port_number>
```
The default port is 8888, however, sometimes it will fail if it is occupied locally. Try any other number above 8000. <br>
For example (my username is bhanda25):
```
ssh bhanda25@scholar.rcac.purdue.edu -L 8868:localhost:8868
```
It will ask for the password, you have to enter your boilerkey password followed with ',push' and confirm with Duo mobile to log in. 
For example: ********,push

After logging in, do <br>
```
module load anaconda
```
```
jupyter lab --port 8868
```
Then copy the url to your favorite browser. It's the best to practice to connect to a remote server via ssh-keys: https://www.rcac.purdue.edu/knowledge/scholar/accounts/login/sshkeys. <br>
# Set up Conda Environment 
For the purpose of this course, we need to be able to access root files. Therefore, installing ROOT is important. However, it is very difficult to install ROOT locally. Instead, we
create Conda Environment and install ROOT within it along with all the packages that are needed for this course.

Go to your scholar notebook terminal, do: <br>
```module load anaconda``` <br>
load a common kernel from the common area, for example, my kernel: <br>
```source activate /depot/cms/conda_envs/bhanda25/Coffea-Santosh``` <br>
then register this kernel to jupyter: <br>
```python -m ipykernel install --user --name=Coffea-Santosh``` <br>
Refresh your notebook then you will see this new kernel with customized conda packages <br>
