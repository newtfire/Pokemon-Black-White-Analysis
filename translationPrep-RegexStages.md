# Regex Replacements for Cleaning up Poke Corpus Scripts

We applied the following steps to clean up the Poke Corpus from English to prepare it for translation to Arabic working with the oXygen XML Editor.
We think these should be the same simple search and replace on any source file that we're preparing for translation. 


1. Remove literal `\n` and `\c` characters:
     * Search: `\\[nc]`
     * Replace: 
      (replaced with a space)

2. Remove extra empty newline characters:
     * Search: `^\n+`
     * Replace `\n`
     (replaced with with a single newline to preserve line boundaries)

3. Found more regex pattern characters to remove:
     * Search: `\\[rv]`
     * Replace:
      (repaced with a space)

4. Remove the literal  `[NULL]` strings.  THIS IS A LITERAL STRING SEARCH, not a regex pattern. Shut off Regular expressions for this.
     * Search: `[NULL]`
     * Replace:
     (repaced with a space)

5. Change the square-bracketted game variables to simplify them as a series of underscores.
     * Search: `\[.+?\]`
     * Replace: `_____`

