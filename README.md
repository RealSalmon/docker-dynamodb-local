## DynamoDb Local

https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.html#DynamoDBLocal.DownloadingAndRunning

```
# The default is to run with the -inMemory arg on port 8000
docker run -it -p 8000:8000 realsalmon/dynamodb-local
```

DynamoDB local accepts the following CLI args

- -cors value — Enable CORS support (cross-origin resource sharing) for 
  JavaScript. You must provide a comma-separated "allow" list of 
  specific domains. The default setting for -cors is an asterisk (*), 
  which allows public access.

- -dbPath value — The directory where DynamoDB will write its database 
  file. If you do not specify this option, the file will be written to 
  the current directory. Note that you cannot specify both -dbPath and 
  -inMemory at once.

- -delayTransientStatuses — Causes DynamoDB to introduce delays for 
  certain operations. DynamoDB can perform some tasks almost 
  instantaneously, such as create/update/delete operations on tables 
  and indexes; however, the actual DynamoDB service requires more time 
  for these tasks. Setting this parameter helps DynamoDB simulate the 
  behavior of the Amazon DynamoDB web service more closely. (Currently, 
  this parameter introduces delays only for global secondary indexes 
  that are in either CREATING or DELETING status.)

- -help — Prints a usage summary and options.

- -inMemory — DynamoDB; will run in memory, instead of using a database 
  file. When you stop DynamoDB;, none of the data will be saved. Note 
  that you cannot specify both -dbPath and -inMemory at once.

- -optimizeDbBeforeStartup — Optimizes the underlying database tables 
  before starting up DynamoDB on your computer. You must also specify 
  -dbPath when you use this parameter.

- -port value — The port number that DynamoDB will use to communicate 
  with your application. If you do not specify this option, the default 
  port is 8000.
  
- -sharedDb — DynamoDB will use a single database file, instead of 
  using separate files for each credential and region. If you specify 
  -sharedDb, all DynamoDB clients will interact with the same set of 
  tables regardless of their region and credential configuration.