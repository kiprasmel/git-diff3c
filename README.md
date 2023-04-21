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
npm i -g yarn diff-so-fancy
```

### install

```sh
git clone https://github.com/kiprasmel/git-diff3c.git
# or:  git clone git@github.com:kiprasmel/git-diff3c.git

cd git-diff3c

./setup-and-update.sh

# https://git-scm.com/docs/git-merge#Documentation/git-merge.txt-mergeconflictStyle
git config --global merge.conflictStyle zdiff3

```

and add to `~/.profile` or equiv:

```sh
export PATH="$(yarn global dir)/node_modules/.bin:$PATH"
```

## usage

```sh
git-diff3c
```

```sh
# specific files
git-diff3c [/path/to/file/with/conflicts[,/another]]
```

