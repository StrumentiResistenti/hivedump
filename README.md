# hivedump
Simple tool to dump hive tables metadata. It requires **Perl** and **Getopts::Long** module only.

    $ ./hivedump -h
    
    Usage: ./hivedump [options] > dump.hql
   
      --database=<db_name>  Specify the DB to export
      --all-databases       Export all databases
      --if-not-exists       Add "IF NOT EXISTS" after "CREATE TABLE"
      --drop-table          Add "DROP TABLE ...;" before "CREATE TABLE"
      --no-location         Suppress LOCATION clause
      --no-partition        Suppress PARTITION information
      --no-tblproperties    Suppress TBLPROPERTIES clause
      --no-stored-as        Suppress STORED AS clause
      --no-row-format       Suppress ROW FORMAT clause
      --help                Prints this information

`hivedump` must be able to execute the `hive` command. Future releases will address `beeline` as an alternative tool and authentication too.
