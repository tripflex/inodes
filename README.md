inodes
======================

Shell/Bash script to display inode count and directory size

## Installation
``` shell
wget -O ~/bin/inodes https://gh.smyl.es/inodes/master/inodes
chmod +x ~/bin/inodes
```

## Usage
Directory path is not required.  If nothing is provided the present working directory is used.
``` shell
inodes /home/user/public_html
```

## Troubleshooting
If you get a "inodes: command not found" you need to set the correct path. In installation above we installed into ~/bin/inodes

Check path with this command and make sure the file is in one of those directories:
``` shell
echo ${PATH}
```

If not you can export path to your .bashrc file
``` shell
PATH=~/bin:"${PATH}"
export PATH
```

And verify
``` shell
which inodes
```