blackman tool
-------------
    - Small package manager which download, compile -if needed- and install
packages from sources.

    - This tool has several goals in mind:
        1. It does not depends on repository.
        2. Be always up to date, since packages builds from
        the very last PKGBUILD in master BlackArch branch.
        3. Download from tool source.
        4. Compile the package.

Usage: blackman 
---------------

OPTIONS:

    PACKAGES:
    -s <pkg>: search package
    -i <pkg>: download and compile package
    -g <group>: install all packages inside a blackarch group
    -a: install all packages from all groups

    REPOSITORY:
    -l: list blackarch groups
    -p <group>: list packages from group
    -u: update system [not implemented yet - v0.X]
    -d: update blackarch repository

    FLAGS:
    -f: force
