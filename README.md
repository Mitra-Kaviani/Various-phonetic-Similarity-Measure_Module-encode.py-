# Various-phonetic-Similarity-Measure_Module-encode.py
Module encode.py - Various phonetic name encoding methods.
Encoding methods provided:
  soundex         Soundex
  mod_soundex     Modified Soundex
  phonex          Phonex
  nysiis          NYSIIS
  dmetaphone      Double-Metaphone
  phonix          Phonix
  fuzzy_soundex   Fuzzy Soundex based on q-gram substitutions and letter
                  encodings
  get_substring   Simple function which extracts and returns a sub-string
  freq_vector     Count characters and put into a vector
See doc strings of individual routines for detailed documentation.
There is also a routine called 'phonix_transform' which only performs the
Phonix string transformation without the final numerical encoding. This can
be useful for approximate string comparison functions.
Note that all encoding routines assume the input string only contains letters
and whitespaces, but not digits or other ASCII characters.
If called from the command line, a test routine is run which prints example
encodings for various strings.
# =============================================================================
  """A 'chooser' functions which performs the selected string encoding method.
  For each encoding method, two calling versions are provided. One limiting the
  length of the code to 4 characters (and possibly pads shorter codes with a
  fill character, for example '0' for soundex), the other returning an
  unlimited length code.
  Possible values for 'encode_method' are:
    soundex           Unlimited length Soundex encoding
    soundex4          Soundex limited/padded to length 4
    mod_soundex       Modified unlimited length Soundex encoding
    mod_soundex4      Modified Soundex limited/padded to length 4
    phonex            Unlimited length Phonex encoding
    phonex4           Phonex limited/padded to length 4
    phonix            Unlimited length Phonix encoding
    phonix4           Phonix limited/padded to length 4
    phonix_transform  Only perform Phonix string transformation without
                      numerical encoding
    nysiis            Unlimited length NYSIIS encoding
    nysiis4           NYSIIS limited/padded to length 4
    dmetaphone        Unlimited length Double-Metaphone encoding
    dmetaphone4       Double-Metaphone limited/padded to length 4
    fuzzy_soundex     Fuzzy Soundex
    fuzzy_soundex4    Fuzzy Soundex limited/padded to length 4
  This functions returns the phonetic code as well as the time needed to
  generate it (as floating-point value in seconds).
  """
