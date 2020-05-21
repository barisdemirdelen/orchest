How Orchest works
=================

Orchest is powered by your filesystem. Upon launching Orchest, Orchest will set a `userdir`
directory (based on the directory in which you launch the application). Inside this directory it
will store the following files:

* Your scripts that make up the pipeline, for example .ipynb files.
* Disktransfer files used by Orchest to pass data between steps (see INSERT ORCHEST SDK).
* Logs to show STDOUT output from scripts in the pipeline view.
* An autogenerated `pipeline.json` file that defines the properties of the pipeline and its steps.
  This includes: execution order, names, images, etc. Without this file Orchest does not work!

Orchest runs completely on docker and only stores a global configuration file. The location for this
config is `~/.config/orchest/config.json` for Unix based systems and `.orchest/config.json` for
Windows.