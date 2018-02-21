
#### PyParanoid 0.2.2

https://pypi.python.org/pypi/PyParanoid/0.2.2

#### inparanoid requires some kind of license:
http://software.sbc.su.se/cgi-bin/request.cgi?project=inparanoid

http://inparanoid.sbc.su.se/cgi-bin/faq.cgi

#### get_homologues
https://github.com/eead-csic-compbio/get_homologues/blob/master/LICENSE.txt

#### Conditional Reciprocal Best BLAST - high confidence ortholog assignment:

https://github.com/cboursnell/crb-blast

notes: http://www.stevekellylab.com/software/conditional-orthology-assignment

#### shmlast: different version of CRB, but uses last rather than BLAST, so is faster

https://github.com/camillescott/shmlast

conda install --file <(curl https://raw.githubusercontent.com/camillescott/shmlast/master/environment.txt)

pip install shmlast

shmlast requires the LAST aligner and gnu-parallel.

#Manually
# LAST can be installed manually into your home directory like so:

cd
curl -LO http://last.cbrc.jp/last-658.zip
unzip last-658.zip
pushd last-658 && make && make install prefix=~ && popd
And a recent version of gnu-parallel can be installed like so:

(wget -O - pi.dk/3 || curl pi.dk/3/ || fetch -o - http://pi.dk/3) | bash
Through a Package Manager
For Ubuntu 16.04 or newer, sufficiently new versions of both are available through the package manager:

sudo apt-get install last-align parallel

#______ synteny

#### allmaps

wget --no-check-certificate https://www.dropbox.com/s/onsjieazu0uytgk/ALLMAPS-install.sh 
sh ALLMAPS-install.sh
cp concorde faSize liftOver ~/bin/









