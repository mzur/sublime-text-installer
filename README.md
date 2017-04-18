# sublime-text-installer

How to build:

1. Update `SUBLIME_VERSION` in `sublime-text-installer.config` and `sublime-text-installer.preinst`
2. Update `SHA256SUM_TGZ` in `sublime-text-installer.config` and `sublime-text-installer.preinst`
3. Update `SUBLIME_VERSION_OLD`. Replace the second number of `seq` with the previous version.
4. Add a new entry to `changelog`. Set the new version name here.
5. Commit the changes.
6. Create a new tag `upstream/VERSION` where `VERSION` is the new version.
7. Run `gbp buildpackage -S`
8. Run `dput ppa:mzur/sublime-text-3 sublime-text-installer_VERSION-1_source.changes` where VERSION is the new version.
9. [Copy](https://askubuntu.com/a/30146/281685) the existing build for other Ubuntu versions.
