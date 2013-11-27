inodes
======================

Shell/Bash script to count and display directory inode usage, and size.  This script will allow you to generate a report of inode usage based off arguments/parameters that you supply.

Prior to 2.0 release a few new features have been added:

Tree display will allow you show sub-directories in the output that have over a specific number of inodes.  So if you want a directory with over 50,000 inodes to display the sub-directories in a tree format, use the -t argument.

Exclude will allow you to exclude directories that are below a specific amount of inodes, therefore creating a smaller output/report.

## Installation
``` bash
wget -O ~/bin/inodes https://raw.smyl.es/inodes/master/inodes
chmod +x ~/bin/inodes
```

## Usage
Directory path is not required.  If nothing is provided the present working directory is used.

Argument | Example | Description
--- | --- | ---
-d | inodes -d /path/to/dir | Specify path to directory to scan.  Optional, will use pwd if not specified.
-t | inodes -t 50000 | Display tree output for directories with over 50,000 inodes.  Optional.
-e | inodes -e 100 | Exclude directories that are below 100 inodes.  Optional

## Examples

Output inode report for /my/dir showing tree output for sub-directories on directories over 50000 inodes

``` bash
inodes -d /my/dir -t 50000
```

Output inode report for /my/dir showing tree output for sub-directories on directories over 50000 inodes, excluding directories with under 10,000 inodes.

``` bash
inodes -d /my/dir -t 50000 -e 10000
```

Output inode report for present working directory without any exclusion or tree output

``` bash
inodes
```

## Troubleshooting
If you get a "inodes: command not found" you need to set the correct path. In installation above we installed into ~/bin/inodes

Check path with this command and make sure the file is in one of those directories:
``` bash
echo ${PATH}
```

If not you can export path to your .bashrc file
``` bash
PATH=~/bin:"${PATH}"
export PATH
```

And verify
``` bash
which inodes
```
