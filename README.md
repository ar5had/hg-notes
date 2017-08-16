# hg-notes
simple notes of mercurial

## exporting patches for more than one commit

For last two rev:

`hg export rev1 rev2`

or 

`hg export -r .^::.`

`.^` stands for the parent of the current commit or you can use rev no here

`.` stands for the current commit

`::` is an operator that says give me all commits between the two ends, both inclusive

check out `hg help revsets` for more

`hg export {multi}` will spit out multiple discrete patches
