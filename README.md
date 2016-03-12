# git tarball

Create a tarball of the git repository. Yes, this is a shortcut for

```
$ git archive --format tar --prefix repo HEAD | gzip > repo.tar.gz
```
with less typing:)

## Install

Just download the script to directory where PATH is set:

```
$ wget https://raw.githubusercontent.com/skaji/git-tarball/master/git-tarball
$ mv git-tarball /path/to/bin/
$ chmod +x /path/to/bin/git-tarball
```

## Usage

```
$ git tarball --help
 Usage: git tarball [options] [commitish]
  -g, --gzip    create tar.gz (default)
  -b, --bzip2   create tar.bz2
  -p, --prefix  create tarball with the prefix, default: top directory name
  -h, --help    show this help

 Examples:
  git tarball                # create tarball with HEAD
  git tarball 0f7fea7        # create tarball with 0f7fea7
  git tarball --bzip         # create tar.bz2
  git tarball --prefix=hello # create hello.tar.gz
```

## Dependencies

* git
* perl 5.8 or later

## License

MIT

## Author

Shoichi Kaji

