![Unfurl Logo](/unfurl/static/unfurl.png)
# Note About This Repo
I (Droogy) forked the [original unfurl repo](https://github.com/obsidianforensics/unfurl) so I could strip it down and use it as a library in a Jupyter Notebook. I patched the core.py module and removed the Flask server and also removed the app and CLI client since they were not necessary for my purposes. I ported the CSV writer and made it an optional feature as well. The notebook ties everything together is very self-explanatory and easy to modify,  
# Extract and Visualize Data from URLs using Unfurl + Jupyter
Unfurl takes a URL and expands ("unfurls") it into a directed graph, extracting every bit of information from the URL and 
exposing the obscured. It does this by breaking up a URL into components, extracting as much information as it can from 
each piece, and presenting it all visually. This “show your work” approach (along with embedded references and documentation) 
makes the analysis transparent to the user and helps them learn about (and discover) semantic and syntactical URL structures.

Unfurl has parsers for URLs, search engines, chat applications, social media sites, and more. It also has more generic parsers 
(timestamps, UUIDs, etc) helpful for exploring new URLs or reverse engineering. It’s also easy to build new parsers, since 
Unfurl is open source (Python 3) and has an extensible plugin system.

No matter if you extracted a URL from a memory image, carved it from slack space, or pulled it from a browser’s history file, 
Unfurl can help you get the most out of it.
## Testing 

1. All tests are run automatically on each PR by Travis CI. Tests need to pass before merging. 
1. While not required, it is strongly encouraged to add tests that cover any new features in a PR. 
1. To manually run all tests (units and integration): ``python -m unittest discover -s unfurl/tests``

If using Docker as above, run: 
``docker exec unfurl python -m unittest discover -s unfurl/tests``

