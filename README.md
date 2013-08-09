cmd_utils
=========

Simple wrapper for subprocess and paramiko to enable simpler command execution both locally and remotely.


## Install ##
```
pip install cmd_utils
```
or
```
python setup.py install
```

## Examples ##
### Local ###
```python
import cmd_utils

working_dir = "/home/mark/a-git-repo"
command = "git diff-index --quiet HEAD --"

output = cmd_utils.run_cmd(command, target_dir)
```
### Remote ###
```python
import cmd_utils

host = "host.example.com"
username = "mark"
working_dir = "/home/mark/a-git-repo"
command = "git diff-index --quiet HEAD --"

output = cmd_utils.run_cmd(host, username, command, working_dir)
```
See `examples.py` for more usage examples.

Versions
--------
* 0.1 - Initial Release