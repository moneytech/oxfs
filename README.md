
# Table of Contents

1.  [oxfs](#orgd85cbd7)
    1.  [usage](#org716fcd5)


<a id="orgd85cbd7"></a>

# oxfs

-   oxfs is a network file system, like sshfs.
-   it is very fast to look up remote files.


<a id="org716fcd5"></a>

## usage

    $ oxfs --help
     usage: oxfs [-h] [-s HOST] [-m MOUNT_POINT] [-r REMOTE_PATH] [-p CACHE_PATH]
                 [-l LOGGING] [-d] [-v]
    
     optional arguments:
       -h, --help            show this help message and exit
       -s HOST, --host HOST  ssh host (for example: root@127.0.0.1)
       -m MOUNT_POINT, --mount_point MOUNT_POINT
                             mount point
       -r REMOTE_PATH, --remote_path REMOTE_PATH
                             remote path, default: /
       -p CACHE_PATH, --cache_path CACHE_PATH
                             oxfs files cache path
       -l LOGGING, --logging LOGGING
                             set log file, default: /tmp/oxfs.log
       -d, --daemon          run in background
       -v, --verbose         print verbose info
    
    $ mkdir remote
    $ oxfs -s user@xxx.xxx.xxx.xxx -m remote -r /home/oxfs -p /tmp/oxfs

