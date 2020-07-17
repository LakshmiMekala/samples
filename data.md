# BE Helm Chart

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square)

Helm chart for BE Applications.

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://kubernetes-charts.storage.googleapis.com/ | efs-provisioner | 0.11.0 |
| https://kubernetes-charts.storage.googleapis.com/ | mysql | 1.6.2 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| as4configmap | object | `{"grid_name":"fd_store","realm_url":"http://localhost:8585","sec_realm_url":"http://localhost:8585","store_poolsize":1,"store_timeout":5,"store_waittime":0.1}` | configmap values for AS4 |
| as4database.GRID_NAME | string | `"grid_name"` |  |
| as4database.REALM_URL | string | `"realm_url"` |  |
| as4database.SEC_REALM_URL | string | `"sec_realm_url"` |  |
| as4database.STORE_POOLSIZE | string | `"store_poolsize"` |  |
| as4database.STORE_TIMEOUT | string | `"store_timeout"` |  |
| as4database.STORE_WAITTIME | string | `"store_waittime"` |  |
| aws-efs.efsProvisioner.awsRegion | string | `"us-east-1"` |  |
| aws-efs.efsProvisioner.efsFileSystemId | string | `"fs-e8f5fa68"` |  |
| aws-efs.enabled | bool | `false` |  |
| aws-efs.replicaCount | int | `1` |  |
| beservice.name | string | `"beservice"` |  |
| beservice.ports.name | string | `"port1"` |  |
| beservice.ports.port | int | `8108` |  |
| beservice.ports.protocol | string | `"TCP"` |  |
| beservice.type | string | `"NodePort"` |  |
| bsType | string | `"na"` |  |
| cacheType | string | `"AS2"` |  |
| cachenode.containers.name | string | `"cachenode"` |  |
| cachenode.name | string | `"becacheagent"` |  |
| cachenode.replicaCount | int | `1` |  |
| cacheservice.name | string | `"becache-service"` |  |
| cacheservice.ports.port | int | `50000` |  |
| cacheservice.ports.protocol | string | `"TCP"` |  |
| cassconfigmap.cass_keyspace_name | string | `"testdb"` |  |
| cassconfigmap.cass_password | string | `"cassandra"` |  |
| cassconfigmap.cass_server_hostname | string | `"localhost"` |  |
| cassconfigmap.cass_server_port | int | `9042` |  |
| cassconfigmap.cass_username | string | `"cassandra"` |  |
| cassdatabase.CASS_KEYSPACE_NAME | string | `"cass_keyspace_name"` |  |
| cassdatabase.CASS_PASSWORD | string | `"cass_password"` |  |
| cassdatabase.CASS_SERVER_HOSTNAME | string | `"cass_server_hostname"` |  |
| cassdatabase.CASS_SERVER_PORT | string | `"cass_server_port"` |  |
| cassdatabase.CASS_USERNAME | string | `"cass_username"` |  |
| cmType | string | `"unclustered"` |  |
| configmap.dbdriver | string | `"com.mysql.jdbc.Driver"` |  |
| configmap.dblogintimeout | int | `0` |  |
| configmap.dbpoolsize | int | `5` |  |
| configmap.dbpwd | string | `"BE_USER"` |  |
| configmap.dburl | string | `"jdbc:mysql://mysql-0.mysql.default.svc.cluster.local:3306/BE_DATABASE"` |  |
| configmap.dbusername | string | `"BE_USER"` |  |
| configmapname | string | `"storeconfig"` |  |
| cpType | string | `"minikube"` |  |
| database.BACKINGSTORE_JDBC_DRIVER | string | `"dbdriver"` |  |
| database.BACKINGSTORE_JDBC_LOGIN_TIMEOUT | string | `"dblogintimeout"` |  |
| database.BACKINGSTORE_JDBC_PASSWORD | string | `"dbpwd"` |  |
| database.BACKINGSTORE_JDBC_POOL_SIZE | string | `"dbpoolsize"` |  |
| database.BACKINGSTORE_JDBC_URL | string | `"dburl"` |  |
| database.BACKINGSTORE_JDBC_USERNAME | string | `"dbusername"` |  |
| ftl.FTL_gv_CLUSTER_NAME | string | `"ftl.default.cluster"` |  |
| ftl.FTL_gv_REALM_SERVER | string | `"http://localhost:8585"` |  |
| ignite.discover_url | string | `"IGNITE_DISCOVER_URL"` |  |
| ignitePort.dis0 | int | `47500` |  |
| ignitePort.dis1 | int | `47501` |  |
| ignitePort.dis2 | int | `47502` |  |
| ignitePort.dis3 | int | `47503` |  |
| ignitePort.dis4 | int | `47504` |  |
| ignitePort.dis5 | int | `47505` |  |
| ignitePort.dis6 | int | `47506` |  |
| ignitePort.dis7 | int | `47507` |  |
| ignitePort.dis8 | int | `47508` |  |
| ignitePort.dis9 | int | `47509` |  |
| image | string | `"ftlsnapp"` |  |
| imagePullPolicy | string | `"IfNotPresent"` |  |
| imagePullSecrets | string | `nil` |  |
| inferencenode.containers.name | string | `"inferencenode"` |  |
| inferencenode.name | string | `"beinferenceagent"` |  |
| inferencenode.replicaCount | int | `1` |  |
| jmxservice.name | string | `"jmx-service"` |  |
| jmxservice.ports.port | int | `5555` |  |
| jmxservice.ports.protocol | string | `"TCP"` |  |
| jmxservice.ports.targetPort | int | `5555` |  |
| jmxservice.type | string | `"LoadBalancer"` |  |
| mysql.args[0] | string | `"--lower_case_table_names=1"` |  |
| mysql.args[1] | string | `"--sql_mode=IGNORE_SPACE,ERROR_FOR_DIVISION_BY_ZERO,NO_AUTO_CREATE_USER,NO_ENGINE_SUBSTITUTION"` |  |
| mysql.enabled | bool | `false` |  |
| mysql.image | string | `"mysql"` |  |
| mysql.imageTag | string | `"5.7"` |  |
| mysql.mysqlDatabase | string | `"BE_DATABASE"` |  |
| mysql.mysqlPassword | string | `"root"` |  |
| mysql.mysqlRootPassword | string | `"password"` |  |
| mysql.mysqlUser | string | `"root"` |  |
| omType | string | `"inmemory"` |  |
| persistentvolumes.openshift.volume.accessModes | string | `"ReadWriteOnce"` |  |
| persistentvolumes.openshift.volume.nfs.sapath | string | `"/home/data/pv0004"` |  |
| persistentvolumes.openshift.volume.nfs.server | string | `"qa.lab.openshift.com"` |  |
| persistentvolumes.openshift.volume.nfs.snpath | string | `"/home/data/pv0003"` |  |
| persistentvolumes.openshift.volume.persistentVolumeReclaimPolicy | string | `"Recycle"` |  |
| persistentvolumes.openshift.volume.savolname | string | `"pv0004"` |  |
| persistentvolumes.openshift.volume.snvolname | string | `"pv0003"` |  |
| persistentvolumes.openshift.volume.storage | string | `"1Gi"` |  |
| storeType | string | `"na"` |  |
| volumes.accessModes[0] | string | `"ReadWriteOnce"` |  |
| volumes.azure.dir_mode | int | `511` |  |
| volumes.azure.file_mode | int | `511` |  |
| volumes.azure.gid | int | `1000` |  |
| volumes.azure.provisioner | string | `"kubernetes.io/azure-file"` |  |
| volumes.azure.skuName | string | `"Standard_LRS"` |  |
| volumes.azure.storageClassName | string | `"azurestorageclass"` |  |
| volumes.azure.uid | int | `1000` |  |
| volumes.saclaimVolume | string | `"pv0004"` |  |
| volumes.samountPath | string | `"/var/lib/mysql"` |  |
| volumes.samountVolume | string | `"sastore"` |  |
| volumes.snclaimVolume | string | `"pv0003"` |  |
| volumes.snmountPath | string | `"/mnt/tibco/be/data-store"` |  |
| volumes.snmountVolume | string | `"store"` |  |
| volumes.storage | string | `"0.5Gi"` |  |
| volumes.storageClass | string | `"standard"` |  |
