# spark-docker

## Validate your cluster

Just validate your cluster accesing the spark UI on each worker & master URL.
Spark Master

    http://localhost:9090/

Spark Worker 1

    http://localhost:9091/

Spark Worker 2

    http://localhost:9092/
    
## after exec into the container 
``` 
cd bin
```

``` 
./spark-sql --master spark://spark-master:7077 --executor-memory 1g --executor-cores 1 --num-executors 1
```

```
CREATE TABLE new USING csv OPTIONS (path '/opt/spark-data/airports.csv', header 'true', inferSchema 'true');
```
