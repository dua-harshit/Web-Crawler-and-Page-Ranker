Python Web Crawler Spider, Page Ranker, and Visualizer

This Web Crawler emulates the crawler function of Search Engine.
then stores the data in a SQLITE3 database named
'spider.sqlite'.  This file can be removed at any time to restart the
process.   

This program crawls a web site and pulls a series of pages into the
database and records the links between pages.

 First step is to run 'spider.py' then enter the page which you want to crawl.

Once you have a few pages in the database, you can run Page Rank on the
pages using the sprank.py program.  Enter how many Page
Rank iterations to run.

You can dump the database using 'spdump.py' to see that page rank has been updated:


You can run sprank.py as many times as you like and it will simply refine
the page rank the more times you run it.  You can even run sprank.py a few times
and then go spider a few more pages sith spider.py and then run sprank.py
to converge the page ranks.

If you want to restart the Page Rank calculations without re-spidering the 
web pages, you can use spreset.py




For each iteration of the page rank algorithm it prints the average
change per page of the page rank.   The network initially is quite 
unbalanced and so the individual page ranks are changing wildly.
But in a few short iterations, the page rank converges.  You 
should run prank.py long enough that the page ranks converge.

To visualize the current top pages in terms of page rank,
run spjson.py to write the pages out in JSON format to be viewed in a
web browser.


Creating JSON output on spider.js...

Enter the no. of nodes
Open force.html in a browser to view the visualization

You can view this data by opening the file force.html in your web browser.  
This shows an automatic layout of the nodes and links.  You can click and 
drag any node and you can also double click on a node to find the URL
that is represented by the node.

This visualization is provided using the force layout from:




