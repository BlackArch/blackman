# ! blackman is not maintained and needs a rewrite, so use at own risk


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
    -n: list native installed blackarch packages
    -p <group>: list packages from group
    -u: update blackarch repository
    -m: upgrade installed packages (-f to reinstall all)

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

    [..]

    [+] Done!

    [ blackarch blackman ]# ls ~/haxx/
    blackarch    forensic       automation   backdoor
    binary       bluetooth      audit        cracker
    crypto       database       debugger     decompiler
    defensive    disassembler   dos          drone
    exploitation fingerprint    firmware     forensic
    fuzzer       hardware       honeypot     keylogger
    malware      misc           mobile       networking
    nfc          packer         proxy        recon
    reversing    scanner        sniffer      social
    spoof        model          tunnel       unpacker
    voip         webapp         windows      wireless
    
    [ blackarch blackman ]# blackman -n
    --==[ blackman - BlackArch ]==--
    [+] beef
        The Browser Exploitation Framework that focuses on the web browser
    [+] bluesnarfer
        A bluetooth attacking tool
    [+] crunch
        A wordlist generator for all combinations/permutations of a given character set.
    [+] dirb
        A web content scanner, brute forceing for hidden files.
    [+] maclookup
        Lookup MAC addresses in the IEEE MA-L/OUI public listing.
    [+] make-pdf
        This tool will embed javascript inside a PDF document.
    [+] maskprocessor
        A High-Performance word generator with a per-position configurable charset.
    [+] netscan
        Tcp/Udp/Tor port scanner with: synpacket, connect TCP/UDP and socks5 (tor connection).
    [+] nipper
        Network Infrastructure Parser
    [+] pdf-parser
        Parses a PDF document to identify the fundamental elements used in the analyzed file.
    ...
