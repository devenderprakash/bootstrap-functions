# hive/glue-sync.sh

Provides function to install Hive Glue Catalog Sync Agent

* [install_glue_sync()](#installgluesync)


## install_glue_sync()

Installs Hive Glue Catalog Sync Agent

Requires Hive 2.x
Currently supported only on AWS

### Example

```bash
install_glue_sync us-east-1
```

### Arguments

* **$1** (string): Region for AWS Athena. Defaults to `us-east-1`

# hive/thrift-metastore.sh

Provides functions to start/stop/restart thrift metastore server

* [start_thrift_metastore()](#startthriftmetastore)
* [stop_thrift_metastore()](#stopthriftmetastore)
* [restart_thrift_metastore()](#restartthriftmetastore)


## start_thrift_metastore()

Function to start thrift metastore server

### Example

```bash
start_thrift_metastore
```

_Function has no arguments._

## stop_thrift_metastore()

Function to stop thrift metastore server

### Example

```bash
stop_thrift_metastore
```

_Function has no arguments._

## restart_thrift_metastore()

Function to restart thrift metastore server

### Example

```bash
restart_thrift_metastore
```

_Function has no arguments._

# hive/ranger-client.sh

Provides function to install Apache Ranger client for Hive

* [install_ranger()](#installranger)


## install_ranger()

Install Apache Ranger client for Hive

Currently supported only on AWS
Requires HiveServer2

### Example

```bash
install_ranger -h example.host -p 6080 -r examplerepo
```

### Arguments

* -h string Hostname of Ranger admin. Defaults to `localhost`
* -p int Port where Ranger admin is running. Defaults to `6080`
* -r string Name of Ranger repository. Defaults to `hivedev`
* -S string Hostname of Solr admin. Defaults to `""`
* -P int Port where Solr admin is running. Defaults to `6083`

# hive/hiveserver2.sh

Provides functions to start/stop/restart HiveServer2

* [is_hs2_configured()](#ishs2configured)
* [stop_hs2()](#stophs2)
* [start_hs2()](#starths2)
* [restart_hs2()](#restarths2)


## is_hs2_configured()

Function to check if HiveServer2 is configured

### Example

```bash
if [[ is_hs2_configured ]]; then
    # do something here
fi
```

_Function has no arguments._

### Exit codes

* **0**: If HiveServer2 is configured
* **1**: Otherwise

## stop_hs2()

Function to stop HiveServer2 JVM

Works on both Hadoop2 and HiveServer2 clusters

### Example

```bash
stop_hs2
```

_Function has no arguments._

## start_hs2()

Function to start HiveServer2 JVM

Works on both Hadoop2 and HiveServer2 clusters

### Example

```bash
start_hs2
```

_Function has no arguments._

## restart_hs2()

Function to restart HiveServer2 JVM

Works on both Hadoop2 and HiveServer2 clusters

### Example

```bash
restart_hs2
```

_Function has no arguments._

