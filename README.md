# ansible-role-nfs-server

### Role Variables Explanation

1. **nfs_server_bind_address** - Defines **the address** on which the *"nfs-server"* will listen on. Defaults to `0.0.0.0`

2. **nfs_server_exports_file_path** - Defines **the path** to [the exports file](https://man7.org/linux/man-pages/man5/exports.5.html). Defaults to `/etc/exports`

3. **nfs_server_nfs_conf_file_path** - Defines **the path** to [nfs.conf](https://www.man7.org/linux/man-pages/man5/nfs.conf.5.html). Defaults to `/etc/nfs.conf`

4. **nfs_server_service_name** - Defaults to `nfs-server`

5. **nfs_server_exports** - A dict of local file systems with a client access control list and options over the "share"
    - **path** - Defines the path to the shared file system
    - **clients** - Defines who can access the share
    - **options** - Defines how the NFS server will share the file system to the clients