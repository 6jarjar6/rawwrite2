# RAWWRITE
Write a binary image to a diskette.
Originally by Mark Becker

Heavily modified by Guy Helmer (4/29/91) to improve performance an add features.

Compiling:
	Appeared to have been written for Turbo C, so I've surrounded
	compiler-specific code in "#if defined(__TURBOC__)" and added
	code in the "#else" clauses for Microsoft C.  Under MSC, code
	should be compiled in the Large memory model.

 Usage:
	MS-DOS prompt> RAWRITE
		and follow the prompts, -or-

	MS-DOS prompt> RAWRITE [-f <file>] [-d <drive>] [-n(owait)] [-h(elp)]
		where:	-f <file> - name of disk image file
			-d <drive> - diskette drive to use, must be A or B
			-n - don't prompt for user to insert diskette
			-h - print usage information to stdout

History
-------

  1.0	-	Initial release
  1.1	-	Beta test (fixing bugs)				4/5/91
  		Some BIOS's don't like full-track writes.
  1.101	-	Last beta release.				4/8/91
  		Fixed BIOS full-track write by only
		writing 3 sectors at a time.
  1.2	-	Final code and documentation clean-ups.		4/9/91
  2.0 (ghelmer@dsuvax.dsu.edu)					4/30/92
  	-	Performance improvements
		Added command line options
		Now compiles under Microsoft C (version 5.1)
