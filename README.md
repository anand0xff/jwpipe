# jwpipe


In 
[JWST Science Calibration Pipeline Overview](https://jwst-docs.stsci.edu/jwst-science-calibration-pipeline-overview) go to [Installation Instructions](https://jwst-pipeline.readthedocs.io/en/stable/)

**miniconda install** Get miniconda.sh installer, copy your ~/.bash_profile and .bashrc to safe names, then (e.g.):

	bash ~/Downloads/Miniconda3-latest-MacOSX-x86_64.sh
	
quit Terminal, restart Terminal (Mac OSX) to reset paths, etc.

	(base) bash$ which conda
	/Users/anand/miniconda3/bin/conda
	(base) bash$ python
	Python 3.11.4 (main, Jul  5 2023, 08:41:25) [Clang 14.0.6 ] on darwin. 
	Type "help", "copyright", "credits" or "license" for more information.
	>>> ^D
	(base) bash$

Install the jwst pipeline:

	conda create -n jwpy311 python
	# add to ~/.bashprofile:   alias  jwpy="conda deactivate; conda activate jwpy311"
	# Now activate jwpy311 (eg using the alias jwpy)
	(jwpy311) bash$  pip install jwst
	
	Add these to ~/.bash_profile to access cal reference database info:
	export CRDS_PATH=$HOME/crds_cache
	export CRDS_SERVER_URL=https://jwst-crds.stsci.edu
	
Install ImPlaneIA:

	bash$ cd ~/.gitsrc
	bash$ git clone git@github.com:anand0xff/ImPlaneIA.git
	bash$ cd ImPlaneIA
	bash$ git checkout centering_RC   # as of 2023_07_12
	bash$ pip install -e .
	

	