
python ~/.local/bin/virtualenv dev_tutorial

source /home/sgordon/repos/envs/dev_tutorial/bin/activate

git clone https://github.com/Zymergen/lab-users.git

cd lab-users/dna-writer

pip install -r requirements.txt

python setup.py install

pip install jupyter

pip list --local

git config --global user.name "zymergen-sgordon"

git config --global user.email "sgordon@zymergen.com"

git config --global credential.helper store

#### see this page for more details on repo checkout:

https://wiki.zymergen.net/display/DEV/Git+notes+for+lab-users

#### run a ipython notebook:
.jupyter folder

Open the 'jupyter_notebook_config.py' file


cd .jupyter

nano jupyter_notebook_config.py

Uncomment line #11 ('c.NotebookApp.port = 8979) and assign a unique port number. Refer to the table in step (4) if you don't have a port number chosen already.


#### shared EC2 instance for Factory personnel who need to use the NGS Pipeline software for preparing, downloading, analyzing, and visualizing next generation sequencing data

zngs-ops-aug

ssh zngs-shared-dev

zngs-ops-aug.zymergen.net


#### from Mike Hamady:


ssh zngs-dev-shared.zymergen.net
