# hg-notes
simple notes of mercurial

## exporting patches for more than one commit

For last two rev:

`hg export rev1 rev2`

or 

`hg diff -r tip~4:tip` for last 4 commits

**Note:** end commit rev no is not inclusive

or

`hg export -r .^::.`

`.^` stands for the parent of the current commit or you can use rev no here

`.` stands for the current commit

`::` is an operator that says give me all commits between the two ends, both inclusive

check out `hg help revsets` for more

`hg export {multi}` will spit out multiple discrete patches

## Enabling extension just for the duration of one command

For example: To use purge without adding it `~/.hgrc`

`hg --config extensions.purge= purge`


## Some useful links
1. https://stackoverflow.com/questions/26544681/how-to-apply-several-patches-using-hg-command-line-when-there-is-already-uncommi

2. https://stackoverflow.com/questions/8188605/mercurial-hg-commit-only-certain-files
