### Commands
1. `$HADOOP_HOME/bin/hdfs dfs -mkdir -p lab1/input`
2. `$HADOOP_HOME/bin/hdfs dfs -put data/users.xml /lab1/input/users.xml`
3. `cd src`
4. `mkdir topten_classes`
5. `javac -classpath $HADOOP_HOME/share/hadoop/common/hadoop-common-2.6.4.jar:$HADOOP_HOME/share/hadoop/mapreduce/hadoop-mapreduce-client-core-2.6.4.jar:$HADOOP_HOME/share/hadoop/common/lib/commons-cli-1.2.jar -d topten_classes sics/TopTen.java`
6. `jar -cvf topten.jar -C topten_classes/ .`
7. `$HADOOP_HOME/bin/hadoop jar topten.jar sics.TopTen lab1/input lab1/ouput`
