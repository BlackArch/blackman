blackman tool
-------------
    Small package manager which download, compile -if needed- and install packages from sources.

    This tool has several goals in mind:
        1. It does not depend on repository.
        2. Be always up to date, since packages builds from the very last PKGBUILD in master BlackArch branch.
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

    SORT TOOLS:
    -h: sort tools into main directory [~/haxx default]
    -D <dir>: change default main directory

    FLAGS:
    -f: force

SORT TOOLS EXAMPLE
-----------------
[ blackarch blackman ]# ./blackman -h
--==[ blackman by nullsecurity.net ]==--
[+] Creating /root/haxx dir for tools

[+] bowcaster tool added to blackarch group
[+] cms-explorer tool added to blackarch group
[+] dirb tool added to blackarch group
[+] flunym0us tool added to blackarch group
[+] netcon tool added to blackarch group
[+] nikto tool added to blackarch group
[+] sploitctl tool added to blackarch group
[+] wnmap tool added to blackarch group
[+] wpscan tool added to blackarch group
[+] xortool tool added to blackarch group
[+] bowcaster tool added to exploitation group
[+] sploitctl tool added to exploitation group
[+] cms-explorer tool added to fingerprint group
[+] cms-explorer tool added to webapp group
[+] dirb tool added to webapp group
[+] flunym0us tool added to webapp group
[+] nikto tool added to webapp group
[+] wpscan tool added to webapp group
[+] dirb tool added to scanner group
[+] flunym0us tool added to scanner group
[+] nikto tool added to scanner group
[+] wnmap tool added to scanner group
[+] wpscan tool added to scanner group
[+] netcon tool added to networking group
[+] nikto tool added to fuzzer group
[+] sploitctl tool added to automation group
[+] wnmap tool added to automation group
[+] xortool tool added to crypto group

[+] Done!

[ blackarch blackman ]# ls ~/haxx/
automation  crypto        fingerprint  networking  webapp
blackarch   exploitation  fuzzer       scanner

[ blackarch haxx ]# tree
.
|-- automation
|   |-- sploitctl -> /usr/share/sploitctl
|   `-- wnmap -> /usr/share/wnmap
|-- blackarch
|   |-- bowcaster -> /usr/share/bowcaster
|   |-- cms-explorer -> /usr/share/cms-explorer
|   |-- dirb -> /usr/share/dirb
|   |-- flunym0us -> /usr/share/flunym0us
|   |-- netcon -> /usr/share/netcon
|   |-- nikto -> /usr/share/nikto
|   |-- sploitctl -> /usr/share/sploitctl
|   |-- wnmap -> /usr/share/wnmap
|   |-- wpscan -> /usr/share/wpscan
|   `-- xortool -> /usr/share/xortool
|-- crypto
|   `-- xortool -> /usr/share/xortool
|-- exploitation
|   |-- bowcaster -> /usr/share/bowcaster
|   `-- sploitctl -> /usr/share/sploitctl
|-- fingerprint
|   `-- cms-explorer -> /usr/share/cms-explorer
|-- fuzzer
|   `-- nikto -> /usr/share/nikto
|-- networking
|   `-- netcon -> /usr/share/netcon
|-- scanner
|   |-- dirb -> /usr/share/dirb
|   |-- flunym0us -> /usr/share/flunym0us
|   |-- nikto -> /usr/share/nikto
|   |-- wnmap -> /usr/share/wnmap
|   `-- wpscan -> /usr/share/wpscan
`-- webapp
    |-- cms-explorer -> /usr/share/cms-explorer
    |-- dirb -> /usr/share/dirb
    |-- flunym0us -> /usr/share/flunym0us
    |-- nikto -> /usr/share/nikto
    `-- wpscan -> /usr/share/wpscan

