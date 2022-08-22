# git-diff3c

when reviewing merge conflicts, especially in a rebase,
it's useful to visualize the diff between
1. old changes -> new old changes (what upstream changed), and
2. old changes -> new changes (what you changed)

## setup

dependencies:
- nodejs
	- yarn (`npm i -g yarn`) 
	- diff-so-fancy (e.g. `npm i -g diff-so-fancy`)

```sh
./setup-and-update.sh
```

## usage

```sh
git-diff3c
```

```sh
# specific files
git-diff3c [/path/to/file/with/conflicts[,/another]]
```

