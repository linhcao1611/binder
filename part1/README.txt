Team members: Linh Cao:       linhcao@csu.fullerton.edu
              Michael Wypych: mwypych@csu.fullerton.edu
	      Tommy Phan:     tommyphan8@csu.fullerton.edu
	      Vinh Ha:	      vha3@csu.fullerton.edu

Execution: "python binder.py <PROGRAM1> <PROGRAM2> ... <PROGRAM N>" e.g. "python binder.py /bin/ls /bin/pwd"
	   "./bound"

Extra Credit: Did not complete


1. Explain what is happening. Do some research in order to nd out what the above copy
command does. In your explanation be sure to explain the role of each argument in the
above command. Also, be sure to explain how Windows handles files which leads to the
above behavior.

The copy command copies the set of files/source (cloud.gif and worm.7z) to a single file specified as destination (result).
The "/B" parameter incates that the set of files are to be binary files.
Since the file "result" contains the binaries for both cloud.gif and worm.7z, depending on the extension we specified
Windows can appropriately open the file using the correct program.

2. How can this technique be used for hiding malicious codes?

This technique can bind malicious programs with actual user programs.  When the user opens the program, they will only see the actual
program and the malicious program will be hidden similar to how we were able to open the .gif file without seeing the malicious
worm.

3. How robust is this technique in terms of avoiding detection by anti-virus tools? You may
need to do some research.

Anti-virus tools use signatures to detect malware.  If the binded malicious binary is known, a decent anti-virus tool will be able to
detect it. And since this technique requires that the malware to be extracted in order to run, a anti-virus should be able to detect it.