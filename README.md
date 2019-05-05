# learning-path-for-coq


## what is coq

Coq is an interactive theorem prover. In another word, you may believe it is a kind of language to prove theorem. I learn it due to function programming. 

https://en.wikipedia.org/wiki/Coq

https://zh.wikipedia.org/wiki/Coq

## install coq in Ubuntu 16.04

The installation of coq may be easier if using Ubuntu 18. Here is for 16.04, which has not direct support to bubblewrap. 

Refer to URLs in the bash below. 

```bash
# install opam (ocaml's package maanger), refer to http://opam.ocaml.org/doc/Install.html
sh <(curl -sL https://raw.githubusercontent.com/ocaml/opam/master/shell/install.sh)

# install pre-req of bubblewrap, refer to https://github.com/tezoscommunity/FAQ/blob/master/Compile_Mainnet.md

sudo add-apt-repository ppa:ansible/bubblewrap
sudo add-apt-repository ppa:git-core/ppa
sudo apt-get update

sudo apt install bubblewrap

# install coq via opam, refer to https://coq.inria.fr/opam-using.html

export OPAMROOT=~/opam-coq.8.9.0 # installation directory
opam init -n --comp=ocaml-base-compiler.4.02.3 -j 2 # 2 is the number of CPU cores
opam repo add coq-released http://coq.inria.fr/opam/released
opam install coq.8.9.0 && opam pin add coq 8.9.0

# install coq IDE
sudo apt install libgtksourceview2.0-dev    # prereq of coq IDE
opam install coqide

```

## run coq, install coq packages 

```bash
export OPAMROOT=~/opam-coq.8.9.0
eval `opam config env`

opam search coq
opam show coq-sudoku
opam install coq-sudoku

```
