# pw_analysis
This is a tool to help with analysis after a full password audit. To use it simply call ```./pw_analysis.py``` and provide it with the list of hashes attempted and potfile from your engagement.
So far it will strip out the basewords from the plaintext passwords in the potfile and count the occurances of those. It will also look for any re-used hashes in the list of hashes attempted. Finally it will create the most common password masks observed from the plaintext passwords to identify patterns in the passwords you were able to crack from the environment.

## Example
```./pw_analysis full_list_of_attempted_hashes.txt engagement_potfile.pot```

## Considerations
It would be best to send this into an output file:

```./pw_analysis full_list_of_attempted_hashes.txt engagement_potfile.pot > analysis.txt```

If you don't want a specific piece of the analysis for some reason simply comment out the function call at the bottom of the file.

This assumes you used Hashcat and your full hashlist is stripped with one hash per line. The potfile is a raw potfile from hashcat.

## TODO
I will be adding more pieces as I get to it, this is more for personal use at this point.
