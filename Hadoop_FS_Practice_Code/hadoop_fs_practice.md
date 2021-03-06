#Hadoop FileSystem Practice Code Snippet

##Basic Hadoop commands
* To list all hadoop fs commands*
```
hadoop fs
```
*To list help of any specific command*
```
hadoop fs -help ls
```
*To list directory*
```
hadoop fs -ls
```
*To create new directory*
```
hadoop fs -mkdir /user/cloudera/sqoop_import
```
*To delete directory*
```
hadoop fs -rm -R
```
*To view data in given file*
```
hadoop fs -cat /user/cloudera/sqoop_import/order_items/part-m-00000
```
*To count data in given file*
```
hadoop fs -cat /user/cloudera/sqoop_import/order_items/part-m-00000 | wc -l
```
*To view occupied disk space*
```
hadoop fs -du -s -h /user/cloudera/sqoopimport/order_items/
```
*To move data from one directory to another*
```
hadoop fs -mv /user/cloudera/sqoop_merge/departments_stage /user/cloudera/sqoop_merge/departments 
```
*To get file(s) from hadoop to local system*
```
hadoop fs -get /user/hive/warehouse/departments/part* .
```
*To put file from local system to hadoop*
```
hadoop fs -put /home/cloudera/departments.avsc /user/cloudera
```
*To view using full NameNode URL*
```
vi /etc/hadoop/conf/core-site.xml (get HadoopFs port from this config)
hadoop fs -ls hdfs://quickstart.cloudera:8020/user/cloudera/tableData/departments
```
