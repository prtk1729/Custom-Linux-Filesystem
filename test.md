### Flow

`NOTE`: FS: Filesystems

- Basic Linux FS information
  - How many lines of code?
  - Download the version and play around with the final product
- Where's Linux FS code?
- Who uses what FS?
- Where do FS sit in the kernel?
- How to get started with FS development?
- Some basic SPFS info?


#### How many FS?
    - Over 80 different file systems.
    - Does linux need all of them?
      - No.
      - But, still there are 30 different filesys invoked during the bootstrap of the OS.
    - Some examples:-
      - Disk-based FS
        - MS FAT
        - ext4
        - NTFS
        - btrfs (`better fs`) 
      - FS with flash memory
      - Distributed FS
      - Dsitributed Parallel FS
      - Encrypted FS

#### What we will learn?
- Build a FileSystem from scratch
- FileSystem operation described one by one
  - mount(8)
  - ls(1) etc
- <kbd> Kernel to FS interactions </kbd>
- Interface with kernel subsystems
  - Buffer cache
  - inode cache
  - page cache
  - dcache etc
- How to add `tracing` to see which filesystem functions are called?
- How to `debug at suorce code` level?
  - To see `kernel stack backtrace` during each sys-call
- Overview and building a filesystem
  - Which `operations come first`, then `which`?


#### Download the source-code and have a look
