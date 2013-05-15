inodes
======================

Shell/Bash script to display inode count and directory size

## Installation
``` bash
wget https://raw.github.com/tripflex/inodes/master/inodes ~/bin/inodes
chmod +x ~/bin/inodes
```

## Usage
Directory path is not required.  If nothing is provided the present working directory is used.
``` bash
inodes /home/user/public_html
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