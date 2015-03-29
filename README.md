Helper script for maintaining the [fedora virt preview repo](http://fedoraproject.org/wiki/Virtualization_Preview_Repository)

When invoked, the script will:

* Check the packages for any updates in fedora dist-git, using fedpkg
* If any packages changed, kick off builds using mock
* Move those builds into the correct directory structure for the repo
* Create the yum repo files
* Upload everything to fedorapeople.org

I run it daily in a cron script.

The initial directory structure can be created for new fedora versions using:

    virtpreview --new-version $VERSION-NUMBER
