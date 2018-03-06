# elasticsearch_kibana
An inventory management example consists of [elasticsearch](https://en.wikipedia.org/wiki/Elasticsearch)/[kibana](https://en.wikipedia.org/wiki/Kibana) + [filebeat](https://www.elastic.co/products/beats/filebeat) + [osquery](https://github.com/facebook/osquery)

## Architecture

   ![resources](https://docs.google.com/drawings/d/e/2PACX-1vTZ25yIVw9eNicVmpLeV8w4jMTVBHMmOejkoc3ojvxKoOTrPv7cfTLCUrVOcUOxvX_vnLBUrZXkYTyB/pub?w=843&h=249)
   
   This example include just one test docker conainer with osquery preinstalled. Other docker containers are for unrelated purpose.
   
## Usage:

### Prepare

1. Install Docker

2. If you are using Docker for Mac or Windows, please allocate enough memory(2GB?) for it because elasticsearch/kibana cost pretty much memory.

3. Download docker-compose.yml and related files https://github.com/jjqq2013/misc/tree/master/elasticsearch6.2.2

    ```
    git clone https://github.com/jjqq2013/misc
    cd misc/elasticsearch6.2.2
    ```
    or if you do not want to clone unrelated files, you can use:
    ```
    svn export https://github.com/jjqq2013/misc/trunk/elasticsearch6.2.2
    cd elasticsearch6.2.2
    ```

### Run

```
docker-compose up
```

Then you can use kibana at http://localhost:5601 to view elasticsearch.

## The cool things of osquery

osquery can be set to output **only changed info** such as new installed packages (of course can send complete info), perioidically.

## The cool things of elasticsearch/kibana6.2.2

All available search keys and values are automatically listed in filter input dialog.
All available search keys and top 5 values are automatically listed in panel.

So you no longer need to input query language for normally.

Here are some snapshots:

<img src="Screen Shot 2018-03-06 at 11.04.32.png">
<img src="Screen Shot 2018-03-06 at 11.09.05.png">
<img src="Screen Shot 2018-03-06 at 11.11.00.png">
<img src="Screen Shot 2018-03-06 at 11.11.15.png">
<img src="Screen Shot 2018-03-06 at 11.11.27.png">
<img src="Screen Shot 2018-03-06 at 11.11.30.png">
<img src="Screen Shot 2018-03-06 at 11.11.32.png">
<img src="Screen Shot 2018-03-06 at 11.11.48.png">
<img src="Screen Shot 2018-03-06 at 11.11.53.png">
<img src="Screen Shot 2018-03-06 at 11.12.02.png">
<img src="Screen Shot 2018-03-06 at 11.12.46.png">
<img src="Screen Shot 2018-03-06 at 11.12.51.png">
<img src="Screen Shot 2018-03-06 at 11.13.24.png">
<img src="Screen Shot 2018-03-06 at 11.13.55.png">
<img src="Screen Shot 2018-03-06 at 11.15.15.png">
<img src="Screen Shot 2018-03-06 at 11.15.21.png">
