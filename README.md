manifest
========

manifest repository to hold (google git-repo) default.xml (and other manifest xml files)

to get started,

```
  $ curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
  $ chmod a+x ~/bin/repo
  $ ~/bin/repo init -m https://github.com/jrmolin/manifest
```


this will download the repo script (a python script), which first pulls the repo bundle from google's
https://gerrit.googlesource.com/git-repo repository (placed in ./.repo/repo).

it also git-clone's this repository into .repo/manifests.git (and then checks out the files to 
.repo/manifests), and sym-links manifests/default.xml to .repo/manifest.xml.

then just run

```
  $ repo sync
```

to cause repo to clone all of the git repositories referenced in default.xml into your working directory.
