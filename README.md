# opam-coq

opam-coq is a dual purpose shell script

  1. a script to install coq starting from zero (it installs opam if needed, then it install itself)
  
  ```
  wget https://raw.githubusercontent.com/gares/opam-coq-shell/master/src/opam-coq
  sh ./opam-coq
  ```
  
  2. a simplified opam shell for the coq user supporting 2 profiles
    1. devel: nothing special for now, just a way to have the right repos configured
    2. user: protected shell around a coq stable version, everything at seen is coq related and stable
    
    ```
    opam coq help # help screen
    opam coq setup 8.5 # installs and pins the last stable version of 8.5
    opam coq seach # only lists coq related packages, only stable packages are at seen
    opam coq install foo # installs foo
    opam coq upgrade # upgrades coq to the last pl of 8.5, that means only bug fixes
    opam coq upgrade foo # upgrades foo to the latest stable version of foo
    ```

# credits
- Thomas Braibant had this idea first

# TODO
- upgrade and install are not coded
- test on OSX or Linux (with no Xcode/gcc installed)
- see if something useful could be added to the devel profile
- check opam >= 1.2
  
