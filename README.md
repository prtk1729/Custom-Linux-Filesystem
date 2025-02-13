# Custom-Linux-Filesystem
PPFS: A custom simple Linux kernel-based filesystem developed from scratch in C. Includes `module creation`, `file operations` and `filesystem design`strategies.
Developed as a final project for C-programming course in IIIT-Hyderabad.


#### Features of the developed filesystem
- Multi-level directories( directories within directories )
- Fixed block size of `2048 blocks`
- Maximum filename length of `28 chars`
- `760 blocks` within filesystem
- Max file-sze of `505 KB`
- `mkfs.ppfs` for formatting filesystem
- `fillfs.ppfs` to populate the filesystem with test files
- `fsdb.ppfs` for file undelete operations
- Supports file `creation`, `deleteion`, `renaming`, `symlinks`

#### Disk Layout
PPFS has a strict disk structure:-
- **Block 0**: PPFS Superblock (2048 bytes)
- **Block 1-128**: Inode table
- **Block 129+**: Data Blocks


#### Installation
##### Building the kernel Module
``` bash
cd kern
make
sudo insmod ppfs.ko
```


##### Creating and Using PPFS
``` bash
mkfs.spfs /dev/sdX
mount -t ppfs /dev/sdX /mnt/ppfs
```

##### Unloading the module
```bash
sudo rmmod ppfs
```

##### Code Structure
- **ppfs.h**: Defines PPFS structures and constants
- **ppfs.c**: Main filesystem operations (mount, unmount, read/write)
- **sp_alloc.c**: Inode and block allocation functions
- **sp_dir.c**: Directory operations
- **sp_inode.c**: Inode management functions
- **sp_file.c**: File operations (read, write etc)
- **sp_ioctl.c**: Special filesystem commands

