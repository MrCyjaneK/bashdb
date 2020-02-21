# bashdb
Minimal key => value file based database.

# Example usage
```
cyjan@root:~$ bashdb
Usage: bashdb [store|delete|read] key [value (only needed in store)]
cyjan@root:~$ bashdb store "my_crazy_key_name/../../../../../../../../../../etc/passwd" "With some stuff inside";
cyjan@root:~$ bashdb read "my_crazy_key_name/../../../../../../../../../../etc/passwd"
With some stuff inside
cyjan@root:~$ ls .bashdb/
my_crazy_key_name_______________________________etc_passwd
cyjan@root:~$ bashdb delete "my_crazy_key_name/../../../../../../../../../../etc/passwd"
cyjan@root:~$ bashdb store "ou" "psie"
cyjan@root:~$ bashdb store "ou" "psie"
[bashdb] > Failed to execute: 'store ou psie', error: it already exist, use 'DELETE' first
cyjan@root:~$ bashdb delete "ou"
cyjan@root:~$ bashdb delete "ou"
[bashdb] > Entry will not get deleted because it didn't exist, imo it's not error so here's 0 exit code.
cyjan@root:~$ 
```

Simply drop bin into your $PATH and chmod +x it.
