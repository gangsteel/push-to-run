# push-to-run
A reinventing-the-wheel project, using git post-receive for automatic deployment

gangsteel, Feb. 22, 2017
Version Beta 0.0

This package is a developing package aimed at automatic job submission to a certain workstation.

Firstly, you have to create a bare git repository and a non-bare git repository on a remote,
where bare repository is used for push,
and non-bare repository is used for deploying your script to run.

In hooks directory, you should create a post-receive script, symlink to the post-receive script
in the working directory (so that user won't be running something they don't know).

You can use the provided post-receive.sample file as a starting point.

Then whenever you push a new change to this bare repository, that script will run,
and that will run the script you write. (In this sample, the printHOST script).
