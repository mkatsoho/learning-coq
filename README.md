# learning-path-for-coq


## what is coq

TBD

## install coq in Ubuntu 16.04

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

# 

```
