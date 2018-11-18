import webbrowser
import sys
 
 
search=raw_input("Quick search:")
search_split=search.split()
 
 
f = open("quicksearch.txt", 'r') 
lines = f.readlines()
 
 
for line in lines:
    line_split=line.split()
    if line_split[1]==search_split[0]:
        b=search_split[1:]
        c=" ".join(b)
        a=line_split[0].replace('AAA',c)
        webbrowser.open(a)
        sys.exit()
 
 
f.close()
 
