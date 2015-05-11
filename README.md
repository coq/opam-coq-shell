# opam-coq

opam-coq is a dual purpose shell script

  1. a script to install coq starting from zero (it installs opam if needed, then it install itself)
  
  ```
  wget https://raw.githubusercontent.com/gares/opam-coq-shell/master/src/opam-coq
  sh ./opam-coq
  ```
  
  2. a simplified opam shell for the coq user supporting 2 profiles
    1. dev: nothing special for now, just a way to have the right repos configured
    2. 8.x: protected shell around a coq stable version, everything at seen is coq related and stable
    
    ```
    opam coq help # help screen
    opam coq init 8.4 # installs and pins the last stable version of 8.4
    opam coq seach # only lists coq related packages, only stable packages are at seen
    opam coq install foo # installs foo
    opam coq upgrade # upgrades coq to the last pl of 8.4, that means only bug fixes
    opam coq upgrade foo # upgrades foo to the latest stable version of foo
    opam coq update # downloads the latest list of packages
    ```

# credits
- Thomas Braibant had this idea first

# TODO
- test on OSX or Linux (with no Xcode/gcc installed)
- see if something useful could be added to the devel profile
- check opam >= 1.2
  
