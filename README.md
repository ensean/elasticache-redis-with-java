
### Demo of connecting to Elasticache Redis(Cluser mode disabled), JDK 11

### File description

```
src/file/redis.properties                               # properties demo for non tls cluster
src/file/redis-tls.properties                           # properties demo for tls cluster
src/main/java/org/example/RedisElasticacheDemo.java     # Demo Java code

```

### Steps to test

1.Build the jar
```
mvn compile assembly:single

```

2.Modify the properties file based on you configuration

3.Run the test

```
export TOOL_CONFIG=/path/to/the/properties
export JARS=/path/to/the/elasticacheredis-demo-1.0-SNAPSHOT-jar-with-dependencies.jar
java -classpath ${JARS} -DCONFIG_FILE_NAME=${TOOL_CONFIG} org.example.RedisElastiCacheDemo
 
```

4.If everything is OK, you should get similar outputs
```shell script
Reading config file...
Completed reading config file.
Initializing Redis client...
SLF4J: Failed to load class "org.slf4j.impl.StaticLoggerBinder".
SLF4J: Defaulting to no-operation (NOP) logger implementation
SLF4J: See http://www.slf4j.org/codes.html#StaticLoggerBinder for further details.
Completed initializing Redis client.
Upserted = {key=Name1, value=Value1}
Upserted = {key=Name2, value=Value2}
Upserted = {key=Name3, value=Value3}
Upserted = {key=Name4, value=Value4}
Upserted = {key=Name5, value=Value5}
Upserted = {key=Name6, value=Value6}
Upserted = {key=Name7, value=Value7}
Upserted = {key=Name8, value=Value8}
Upserted = {key=Name9, value=Value9}
Upserted = {key=Name10, value=Value10}
Upserted = {key=Name11, value=Value11}
Upserted = {key=Name12, value=Value12}
Upserted = {key=Name13, value=Value13}
Upserted = {key=Name14, value=Value14}
Upserted = {key=Name15, value=Value15}
Upserted = {key=Name16, value=Value16}
Upserted = {key=Name17, value=Value17}
Upserted = {key=Name18, value=Value18}
Upserted = {key=Name19, value=Value19}
Upserted = {key=Name20, value=Value20}
Upserted = {key=Name21, value=Value21}
Upserted = {key=Name22, value=Value22}
Upserted = {key=Name23, value=Value23}
Upserted = {key=Name24, value=Value24}
Upserted = {key=Name25, value=Value25}
Upserted = {key=Name26, value=Value26}
Upserted = {key=Name27, value=Value27}
Upserted = {key=Name28, value=Value28}
Upserted = {key=Name29, value=Value29}
Upserted = {key=Name30, value=Value30}
Upserted = {key=Name31, value=Value31}
Upserted = {key=Name32, value=Value32}
Upserted = {key=Name33, value=Value33}
Upserted = {key=Name34, value=Value34}
Upserted = {key=Name35, value=Value35}
Upserted = {key=Name36, value=Value36}
Upserted = {key=Name37, value=Value37}
Upserted = {key=Name38, value=Value38}
Upserted = {key=Name39, value=Value39}
Upserted = {key=Name40, value=Value40}
Upserted = {key=Name41, value=Value41}
Upserted = {key=Name42, value=Value42}
Upserted = {key=Name43, value=Value43}
Upserted = {key=Name44, value=Value44}
Upserted = {key=Name45, value=Value45}
Upserted = {key=Name46, value=Value46}
Upserted = {key=Name47, value=Value47}
Upserted = {key=Name48, value=Value48}
Upserted = {key=Name49, value=Value49}
Upserted = {key=Name50, value=Value50}
Retrieved value='Value21' for key= 'Name21' in 1 millisecond(s).
Deleted key 'Name12'
Testing delete...
Key 'Name12' not found.
Completed testing delete.
Shutting down Redis client...
Completed shutting down Redis client.
```

### Credits

Credits to [amazon-elasticache-redis-and-memcached-java-client-examples](https://github.com/aws-samples/amazon-elasticache-redis-and-memcached-java-client-examples.git)