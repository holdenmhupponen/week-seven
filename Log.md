<img width="840" height="840" alt="image" src="https://github.com/user-attachments/assets/d49c54d5-7709-4b44-ae44-482e35266dd2" /># Roman Networks Colab Project
- successfully installed preliminaries - no error
- successfully grabbed the data and saved to the .csv files - no error
- successfully plotted the graph - no error:
  - <img width="1189" height="790" alt="image" src="https://github.com/user-attachments/assets/f56d70a2-ee25-4d7b-a0a9-75cf2dbba40e" />
- tried to run the degree calculation under measuring a network but faced an error:
  - "NameError: name 'networkx' is not defined"
  - I think this is because the initial preliminaries section had "import networkx as nx" so it should be nx?
  - yes; I changed it to nx.degree and it worked
- successfully made a table ranked by the highest number of connections or "degree" - no error
  - I believe the significance of these cities/settlements is that they are historically important trading ports, which would mean many more connections than other such cities/settlements; it seems to represent the Early Roman Republic due to the significance of Carthage there
- successfully made the betweenness centrality graph - no error
  - from my understanding, the higher betweenness values represents a node's being more likely to be used between two other points - a sort of middle man measurement of the cities that are most used as halfway points
  - I notice Rhodos and Lilybaeum appearing again: this might suggest that their high number of connections is less so due to their own merits and more so due to their positions between other cities/settlements?
- successfully made the modularity graph - no error
  - from my reading of the documentation, I believe that "greedy" refers to the fact that the function looks for the biggest modularity values and takes it to its endpoint instead of worrying about what it could end up as? as in how a greedy person might accept a briefcase of cash without worrying about whether it's wiretapped - so too does the algorithm look for the biggest values right now with horseblinders on.
  - the modularity score was 0.814 - so, pretty good I'd say
  - found that Roma is in community 3
- successfully plotted the networks but now coloured by communities - no error:
  - <img width="1206" height="790" alt="image" src="https://github.com/user-attachments/assets/a09242b4-3f51-402b-a797-f646d41b8c22" />
- successfully plotted just the 3rd community; or, Rome's community - no error:
  - <img width="989" height="790" alt="image" src="https://github.com/user-attachments/assets/a1cd76d8-fe8a-4fef-b18e-46907112c4a7" />
  - it seems to me that the high modularity score would suggest a high level of connection between the communities; that the Roman system of settlements/cities was more like different localized clusters than the highly disparate cities of modern, centralized nations today.
  - further, the cities in Rome's community seem to be mostly limited to the western empire near Rome itself - there don't seem to be any Greek/Anatolian/African/etc. cities
 
# Network Navigator
- typed up the family names with their birth and death years into notepad, saved as .csv
- imported into networknavigator:
  - <img width="1192" height="634" alt="image" src="https://github.com/user-attachments/assets/f025c506-168a-47be-9dfe-2abbca9a78fd" />
- it shows me that the years with the most connections are 1875, with three, and 1850, 1825 and 1848 each with two

# Google Colab Project
- loaded everything correctly, installed the preliminaries - no error
- came across an error when I tried to calculate the closeness centrality
  - it seems that there were values in my .csv files that were NAN, which didn't work
  - I typed my error into Google and found this thread on stackoverflow: https://stackoverflow.com/questions/22016166/remove-or-find-nan-in-r
  - used this in my code with the line "closeness_cent\[is.nan(closeness_cent)] <- 0" to turn all the nan values into 0
  - worked:
    - <img width="840" height="840" alt="image" src="https://github.com/user-attachments/assets/b2b76f5c-ebd1-4f1f-9c08-748c92072ed0" />
    - <img width="840" height="840" alt="image" src="https://github.com/user-attachments/assets/928f3c75-6786-4be0-a836-66c7247be8b4" />
- put the code in to calculate the betweenness centrality - there was an error message but it seemed not to effect much:
  - "Warning message:
    “`as.undirected()` was deprecated in igraph 2.1.0.
    ℹ Please use `as_undirected()` instead.”
  - <img width="840" height="840" alt="image" src="https://github.com/user-attachments/assets/ec549994-472e-4244-971b-729f595716ac" />
  - <img width="840" height="840" alt="image" src="https://github.com/user-attachments/assets/a0da7db8-1d39-47ec-9325-affc57b310d3" />
- successfully calculated and printed the modularity score ("0.7234375") - no error
- successfully graphed the distribution of community sizes and the network communities
  - <img width="840" height="840" alt="image" src="https://github.com/user-attachments/assets/a99f0e20-a6da-45f7-a5a0-ee284c9cc1b9" />
  - <img width="840" height="840" alt="image" src="https://github.com/user-attachments/assets/d1d27e01-acc0-4288-adad-e840d2e9eb5d" />
