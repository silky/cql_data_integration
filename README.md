# cql_data_integration
Interface for generating Categorical Query Language files to merge/migrate data between databases

# Setup
```
cd cql_data_integration
python3 -m venv .env
source .env/bin/activate
pip install -r requirements.txt
```

Furthermore, to execute CQL files generated by the science example, a MySQL database connection OQMD (version 1.1) must be made available (it can be downloaded from [here](http://www.oqmd.org/download/)). Supporting MySQL alone for external databases is a limitation of this interface, not of CQL. The input files can be modified to allow one to write in the database connection info.

# Usage

CQL files can be generated by executing the `cdi/library_example/main.py` and `cdi/science_example/main.py` scripts from the command line.

Something like the following alias might be useful for allowing CQL to interact with databases as well as use user-defined functions.

`alias runcql='java -Xmx4096m -cp "/some/path/to/mysql-connector-java-5.1.47.jar:~/cql_data_integration/aql.jar:~/cql_data_integration/scripts/bin" catdata.ide.IDE'`

The non-scientific example is much simpler and relies on no external databases, so it may be a better starting point.
