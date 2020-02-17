# pg_partitions 

The `pg_partitions` system view is used to show the structure of a partitioned table.

|column|type|references|description|
|------|----|----------|-----------|
|`schemaname`|name| |The name of the schema the partitioned table is in.|
|`tablename`|name| |The name of the top-level parent table.|
|`partitionschemaname`|name| |The namespace of the partition table.|
|`partitiontablename`|name| |The relation name of the partitioned table \(this is the table name to use if accessing the partition directly\).|
|`partitionname`|name| |The name of the partition \(this is the name to use if referring to the partition in an `ALTER TABLE` command\). `NULL` if the partition was not given a name at create time or generated by an `EVERY` clause.|
|`parentpartitiontablename`|name| |The relation name of the parent table one level up from this partition.|
|`parentpartitionname`|name| |The given name of the parent table one level up from this partition.|
|`partitiontype`|text| |The type of partition \(range or list\).|
|`partitionlevel`|smallint| |The level of this partition in the hierarchy.|
|`partitionrank`|bigint| |For range partitions, the rank of the partition compared to other partitions of the same level.|
|`partitionposition`|smallint| |The rule order position of this partition.|
|`partitionlistvalues`|text| |For list partitions, the list value\(s\) associated with this partition.|
|`partitionrangestart`|text| |For range partitions, the start value of this partition.|
|`partitionstartinclusive`|boolean| |`T` if the start value is included in this partition. `F` if it is excluded.|
|`partitionrangeend`|text| |For range partitions, the end value of this partition.|
|`partitionendinclusive`|boolean| |`T` if the end value is included in this partition. `F` if it is excluded.|
|`partitioneveryclause`|text| |The `EVERY` clause \(interval\) of this partition.|
|`partitionisdefault`|boolean| |`T` if this is a default partition, otherwise `F`.|
|`partitionboundary`|text| |The entire partition specification for this partition.|
|`parenttablespace`|text| |The tablespace of the parent table one level up from this partition.|
|`partitiontablespace`|text| |The tablespace of this partition.|

**Parent topic:** [System Catalogs Definitions](../system_catalogs/catalog_ref-html.html)
