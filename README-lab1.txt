README-lab1.txt
===============

NOTE: some mistakes in this document are done on purpose :)

* Clone the repo
  $ git clone https://github.com/StreamUnlimited/training-git.git

* Create topic branch
  $ git branch RDO-fix
  $ git checkout RDO-fix

* Fix a mistake in the provided matterials and commit it
  $ git gui

* Create a bare repo on the USB stick
  $ cd /media/rdostal/1234-5678/
  $ mkdir git-training.git
  $ cd git-training.git
  $ git init --bare

* Push your change to the bare repo
  $ git remote add RadekUSB /media/rdostal/1234-5678/git-training.git
  $ git push RadekUSBstick RDO-fix

* Give the USB stick to the person on the right

* Add remote from USB stick and fetch changes from there
  $ git remote add ....
  $ git fetch --all

* If you find change provided on the USB stick useful and according to
  the guidelines, please export the patch and send it to
  radek.dostal@streamunlimited.com

* Create your own pre merge branch RDO-pre-merge from master
  * Quick
    $ git checkout -b RDO-pre-merge master
  * Stupid proof
    $ git checkout master
    $ git branch RDO-pre-merge
    $ git checkout RDO-pre-merge

* Merge both branches into RDO-pre-merge
  * First merge your own branch from command line
    $ git merge ...
  * Merge the remote branch using the UI and review the incoming patches

* Inspect the results using git blame
  $ git blame README-lab1.txt

* Inspect the history using gitk
  $ gitk --all
