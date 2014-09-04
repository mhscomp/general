#MHS Robotics Club: GIT#

In order to clone a repository into a local copy:
```bash
$ git clone https://path/to/remote/repository
```
Once you have made changes to the local copy, you add all of the files.
```bash
$ git add -A
```

Then, commit the changes:
```bash
$ git commit -m "desciption of changes"
```

If you don't want a file to have its changes tracked (for example, `text.txt`), create a `.gitignore` file directly inside the repository with a format like this:

```
text.txt
some_file_that_you_dont_want_tracked.js
otherfile.html
```

Finally, to push the changes:
```bash
$ git push
```

<b>Next Step: <a href="example.md">Example</a></b>