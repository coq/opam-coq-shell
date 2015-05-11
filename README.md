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
	Please run:
	  opam coq init <profile>

	Available profiles:

	  8.4
	    A stable system, version 8.4, with easy install
	    of stable packages in a simplified opam shell.
	    Recommended profile for beginners (non OPAM experts).
	    Possibility to upgrade the system followin bug-fix
	    releases of Coq 8.4

	  dev
	    Full control.  This profile simply adds all official
	    coq related package repositories (both stable and
	    unstable ones).
    ```

    Once `init` has been run, the `8.x` profile help screen is:
		
    ```
    Supported commands are:
      opam coq help
        this screen
    
      opam coq seach <keyword>
        searches the list of known coq packages for a package maching <keyword>
    
      opam coq install <package>
        installs the given package
    
    	opam coq update
    	  update the list of available packages
    
      opam coq upgrade <package>
        if <package> is omitted, then it upgrades coq the the last bugfix release
        if <package> if given, it updates such package to the last stable release
    ```

# credits
- Thomas Braibant had this idea first

# TODO
- test on OSX or Linux (with no Xcode/gcc installed)
- see if something useful could be added to the devel profile
- check opam >= 1.2
  
