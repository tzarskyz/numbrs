# numbrs

See the line numbers of whathever it is that's going on in STDOUT by piping it to `numbrs`.

## Instalation:

The only requirement for this script is perl, which, if you're using Linux, you most certainly
already have.
Just put the file in one of the many paths that your `$PATH` already has, hopefully, you'll have
write access to one of them to put the file there and give it execution permission, basically this:

    $ mv numbrs ~/bin
    $ chmox +x ~/bin/numbrs

## Example usage:

### Number `ls` output:

    $ ls -1
    README.md
    numbrs
    $ ls -1 | numbrs
    1 README.md
    2 numbrs

### Number `grep` output:

    $ grep "num" README.md | numbrs
    1 numbrs
    2 See the line numbers of whathever it is that's going on in STDOUT by piping it to `numbrs`.
    3     cat numbrs | ./numbrs
    4     numbrs
    5     $ ls -1 | numbrs
    6     2 numbrs

### Number `cat` output:

    $ cat .git/config | numbrs
    1 [core]
    2   repositoryformatversion = 0
    3   filemode = true
    4   bare = false
    5   logallrefupdates = true
    6 [remote "origin"]
    7   url = git@github.com:LuRsT/numbrs.git
    8   fetch = +refs/heads/*:refs/remotes/origin/*
    9 [branch "master"]
    10  remote = origin
    11  merge = refs/heads/master

