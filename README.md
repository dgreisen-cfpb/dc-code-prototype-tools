dc-code-prototype-tools
=======================

Tools for creating the files in the dc-code-prototype repository.

* parse_code_2013-10.py: Parses the [.docx file provided by Lexis](https://github.com/vzvenyach/Code_PrimaryDocs/blob/master/PrimaryDocs/DC_Code_Sept_2013.docx) in October 2013 into XML.
* parse_code_2012-12.py: Parses the [Word documents provided by West](http://dccouncil.us/UnofficialDCCode) for the December 2012 edition of the DC Code into XML. Convert the .doc files to .docx first using `libreoffice --headless --convert-to docx *.doc`.
* worddoc.py: This module contains a function called open_docx(filename) which opens a .docx file and returns a simplified data structure for document content, with error checking for elements that it does not recognize. Used by parse_code_2013-10.py and parse_code_2012-12.py.
* compare_helper.py: Normalizes various parts of the DC Code XML so that the XML derived from the 2012 West file and the XML derived from the 2013 Lexis file can be compared more easily using `diff`.
* split_up.py: Splits the final XML into many smaller files in the way I created the dc-code-prototype repository, and creates a top-level table of contents file (toc.xml).
