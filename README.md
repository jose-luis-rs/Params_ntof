# Purpose

The R3BRoot software is based on the FairRoot framework and can be used to perform Monte Carlo simulations and experimental data analysis of the R3B (Reactions with Relativistic Radioactive Beams) nuclear physics experiments at the FAIR research center (Facility for Antiproton and Ion Research).

This repository contains all the parameters, root geometries and input files needed for n_TOF simulation based on the R3BRoot software.

# Download

~~~bash
git clone git@github.com:jose-luis-rs/Params_ntof.git
cd Params_ntof
git checkout dev
~~~

# Developers

First, fork the main repository of parameters from the GitHub account and then download it as follows

~~~bash
git clone https://github.com/user_name/Params_ntof.git
cd Params_ntof
git checkout dev
~~~

Now when your origin points to your fork. You need to add the main repo to your remotes as well. You should have "origin --> you fork" and "mainrepo --> the main repo".

~~~bash
git remote add mainrepo git@github.com:jose-luis-rs/Params_ntof.git
git fetch mainrepo
~~~

Sync your feature branch

As often as possible sync your feature branch with the central dev.

  Sync:
~~~bash
    git fetch mainrepo
    git checkout feature_branch
    git rebase mainrepo/dev
~~~
- Resolve conflicts if any.
- Stage each modified file "git add <file_name>" after conflicts are resolved.
- You can also use "git checkout --theirs/--ours " to help to resolve conflicts.
- Use "git rebase --continue" to continue rebasing.

  Push to your remote clone:
~~~bash
    git push origin
~~~

# Configuration
Before running your analysis macros, load the path to parameter files using the config.sh script:
~~~bash
source config.sh 
~~~
