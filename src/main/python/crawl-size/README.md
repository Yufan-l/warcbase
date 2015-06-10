This program launches a simple web server that provides a breakdown of domains per each crawl file - it lets you quickly see, at a glance, how your corpus changes over time. Mouseovers allow you to match the legend to the content bars themselves.

To run, you need to process the output of your basic crawl statistics script to count the number of pages per domain. For more, see the second script at <https://github.com/lintool/warcbase/wiki/Pig:-Gathering-Basic-Crawl-Statistics>. To process, use the following:

```
./process.py <INPUT> > data.csv
```

For example,

```
./process.py part-m-00000 > data.csv
```

You then want to start a simple server to generate the visualization. Run the following from this directory:

```
python -m SimpleHTTPServer 1234
```

1234 represents the port number. If you use 1234, you can find the visualization at <http://localhost:1234>. Feel free to change the port number as appropriate.

From: http://bl.ocks.org/mbostock/3886208

