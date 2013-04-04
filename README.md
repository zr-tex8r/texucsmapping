texucsmapping Package
=====================

Files describing mappings from various LaTeX mappings to Unicode.

  * File `bx-xxx.txt` contains the mapping from XXX to Unicode.
  * Currently supported encodings:  
    IL2, L7x, LY1, OML, OMS, OMX, OT1, OT2, OT4, QX, T1,
    T2A, T2B, T2C, T5, TS1
  * Not (yet) supported important encodings:  
    LGR, T3

### File Format

Lines starting with `#` are comment lines. a non-comment line
shows a mapping of a character and is of the following form:

    0x27    0x2019  #(quoteright)RIGHT SINGLE QUOTATION MARK
    ~~~~A   ~~~~~~B  ~~~~~~~~~~~C~~~~~~~~~~~~~~~~~~~~~~~~~~~D

  * A: codepoint in the source (LaTeX) encoding
  * B: codepoing in Unicode
  * C: glyph name, given in the following cases:
      - The name is registered in Adobe Glyph List For New Fonts.
      - The character is in PUA.
  * D: Unicode character name (or `<PUA>` if so)

### PUA Repositories

The mappings in this package give high priority to one-to-one
correspondence between the source encoding and Unicode. Thus when
the source character is not contained (as-is) in current Unicode
Standard, then characters from some PUA repositories are employed.
Note that being one-to-one is preferred over the conformance to the
Unicode Standard, so ocasionally glyphs that should be seen as
representable (by combining sequences, as glyph variants, etc.) are
encoded as a PUA character.

The following PUA repositories are employed (in the descending order
of priority):

 1. Adobe's (obsolete) repository
 2. codepoints used in the Latin Modern font family
 3. the author's private repository

### Revision History

  * Version 0.2 <2013/04/05>
      - First public version.

--------------------
Takayuki YATO (aka. "ZR")  
http://zrbabbler.sp.land.to/
