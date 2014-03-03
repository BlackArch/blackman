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
    
    [ blackarch haxx ]# tree
    .
    |-- automation
    |   |-- sploitctl -> /usr/share/sploitctl
    |   `-- wnmap -> /usr/share/wnmap
    |-- blackarch
    |   |-- bletchley -> /usr/share/bletchley
    |   |-- bowcaster -> /usr/share/bowcaster
    |   |-- cms-explorer -> /usr/share/cms-explorer
    |   |-- dirb -> /usr/share/dirb
    |   |-- dns2tcp -> /usr/share/dns2tcp
    |   |-- fakedns -> /usr/share/fakedns
    |   |-- flunym0us -> /usr/share/flunym0us
    |   |-- icmptx -> /usr/share/icmptx
    |   |-- inguma -> /usr/share/inguma
    |   |-- js-beautify -> /usr/share/js-beautify
    |   |-- netcon -> /usr/share/netcon
    |   |-- netdiscover -> /usr/share/netdiscover
    |   |-- nikto -> /usr/share/nikto
    |   |-- peepdf -> /usr/share/peepdf
    |   |-- ropeme -> /usr/share/ropeme
    |   |-- ropgadget -> /usr/share/ropgadget
    |   |-- secure-delete -> /usr/share/secure-delete
    |   |-- sploitctl -> /usr/share/sploitctl
    |   |-- thc-ipv6 -> /usr/share/thc-ipv6
    |   |-- udptunnel -> /usr/share/udptunnel
    |   |-- wnmap -> /usr/share/wnmap
    |   |-- wpscan -> /usr/share/wpscan
    |   |-- xorbruteforcer -> /usr/share/xorbruteforcer
    |   `-- xortool -> /usr/share/xortool
    |-- cracker
    |   `-- inguma -> /usr/share/inguma
    |-- crypto
    |   |-- bletchley -> /usr/share/bletchley
    |   |-- xorbruteforcer -> /usr/share/xorbruteforcer
    |   `-- xortool -> /usr/share/xortool
    |-- defensive
    |   `-- secure-delete -> /usr/share/secure-delete
    |-- disassembler
    |   `-- inguma -> /usr/share/inguma
    |-- dos
    |   `-- thc-ipv6 -> /usr/share/thc-ipv6
    |-- exploitation
    |   |-- bowcaster -> /usr/share/bowcaster
    |   |-- inguma -> /usr/share/inguma
    |   |-- ropeme -> /usr/share/ropeme
    |   |-- ropgadget -> /usr/share/ropgadget
    |   |-- sploitctl -> /usr/share/sploitctl
    |   `-- thc-ipv6 -> /usr/share/thc-ipv6
    |-- fingerprint
    |   `-- cms-explorer -> /usr/share/cms-explorer
    |-- forensic
    |   |-- peepdf -> /usr/share/peepdf
    |   `-- secure-delete -> /usr/share/secure-delete
    |-- fuzzer
    |   `-- inguma -> /usr/share/inguma
    |-- malware
    |   `-- peepdf -> /usr/share/peepdf
    |-- networking
    |   |-- netcon -> /usr/share/netcon
    |   |-- thc-ipv6 -> /usr/share/thc-ipv6
    |   `-- udptunnel -> /usr/share/udptunnel
    |-- proxy
    |   `-- fakedns -> /usr/share/fakedns
    |-- recon
    |   `-- netdiscover -> /usr/share/netdiscover
    |-- reversing
    |   `-- js-beautify -> /usr/share/js-beautify
    |-- scanner
    |   |-- dirb -> /usr/share/dirb
    |   |-- flunym0us -> /usr/share/flunym0us
    |   |-- inguma -> /usr/share/inguma
    |   |-- nikto -> /usr/share/nikto
    |   |-- wnmap -> /usr/share/wnmap
    |   `-- wpscan -> /usr/share/wpscan
    |-- spoof
    |   `-- fakedns -> /usr/share/fakedns
    |-- tunnel
    |   |-- dns2tcp -> /usr/share/dns2tcp
    |   |-- icmptx -> /usr/share/icmptx
    |   `-- udptunnel -> /usr/share/udptunnel
    |-- unpacker
    |   `-- js-beautify -> /usr/share/js-beautify
    |-- webapp
    |   |-- cms-explorer -> /usr/share/cms-explorer
    |   |-- dirb -> /usr/share/dirb
    |   |-- flunym0us -> /usr/share/flunym0us
    |   |-- nikto -> /usr/share/nikto
    |   `-- wpscan -> /usr/share/wpscan
    `-- wireless
        `-- netdiscover -> /usr/share/netdiscover

    
