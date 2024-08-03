# Yet-Another-Distributed-File-System

## Setting up YADFS

Setup the Distributed File System. The configuration to setup a distributed file system is provided in the config_sample.json file.
```
usage: setup.py [-h] --CONFIG CONFIG [--CLEANUP CLEANUP]

Setup the DFS

optional arguments:
-h, --help            show this help message and exit
--CONFIG CONFIG, -f CONFIG
                        Path to the config file
--CLEANUP CLEANUP, -c CLEANUP
                        Overwrite existing DFS
```

Example:
```
python3 setup.py --CONFIG config_sample.json --CLEANUP True
```

Running the setup.py script will generate a configuration file to load the distributed file system from. A sample one is provided in dfs_setup.json. Run the CLI to access the distributed file system.
```
usage: yadfs.py [-h] --CONFIG CONFIG

Load up the DFS

optional arguments:
-h, --help            show this help message and exit
--CONFIG CONFIG, -f CONFIG
                        Path to the DFS config file
```

Example:
```
python3 yadfs.py --CONFIG dfs_setup.json
```

## Manipulating YADFS
The following commands can be run on YADFS. Only use absolute paths.

Move a file to the distributed file system
```
usage: put SOURCE_FILE_IN_LOCAL DESTINATION_FILE_IN_DFS
```

Create a directory in the distributed file system
```
usage: mkdir DIR_NAME
```

Remove a file from the distributed file system
```
usage: rm FILE_NAME
```

Remove a directory recursively from a distributed file system
```
usage: rmdir DIR_NAME
```

View the contents of a file in the distributed file system
```
usage: cat FILE_NAME
```

List all the files and folders in a directory in the distributed file system
```
usage: ls DIR_NAME [-r RECURSIVE]
```

Formats contents of the namenode and datanode
```
usage: format
```
