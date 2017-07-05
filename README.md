ctrans.py
---------

very crude source code comment translator. powered by google translate.

currently handles C-style and scripting-style (i.e. '#') comments; note that
comments formatted as '### comment' will still end up as '# comment', this
is a bug i don't care about fixing atm; i'm more concerned with just getting
this working.


USAGE:
    ctrans.py -s <filename>
    translates a single file

    ctrans.py -d <dir>
    translates all source files in a directory
    
    other flags:
        -e      set input file encoding
        -o      set output file encoding
        --t      set trace (debugging output)
        --srclang force input language
        --tolang set output language
        --ext change translate file extension (by default, a copy is made with name src.tolang e.g: index.ts -> index.ts.en) 

DECODE/ENCODE NOTES:
    the default encoding and decoding is utf-8. specifying 'auto' for the
    decoding will attempt to guess the file's encoding. this is at best a guess,
    and at worst completely wrong.
    
    encoding is not a trivial matter, and there are a million ways a file might
    be encoded. 

TODO:
    * add directory-translating mode
    * add support for multiline C comment
    * verify code is clean, was hacked together in a hurry
    
