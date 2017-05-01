
vlmcsd - portable open-source KMS Emulator in C

Supported operating systems / run-time environments
        Linux, GNU/Linux, uclibc/Linux, musl/Linux, Android (bionic/Linux), FreeBSD, FreeBSD with glibc (e.g. debian/kFreeBSD), OpenBSD, NetBSD, DragonflyBSD, Solaris, Open Indiana, Dyson, Minix, Darwin, Mac OS, iOS, Windows, Cygwin, WSL, Wine, The Hurd.
    Supported CPUs
        x86, arm, mips, PowerPC, Sparc, s390


vlmcsd is

    a replacement for Microsoft's KMS server
    It contains vlmcs, a KMS test client, mainly for debugging purposes, that also can "charge" a genuine KMS server
    designed to run on an always-on or often-on device, e.g. router, NAS Box, ...
    intended to help people who lost activation of their legally-owned licenses, e.g. due to a change of hardware (motherboard, CPU, ...)

vlmcsd is not

    a one-click activation or crack tool
    intended to activate illegal copies of software (Windows, Office, Project, Visio)

CHANGES

    2017-01-19 (1108)
        Fixed a bug that Android x86/x64 builds terminated with SIGILL (illegal instruction) if run from a non-Atom CPU (thx to Daz)
        New option -x1 (requested by Hahu) that causes vlmcsd to exit if
            any of the listening sockets (IP address / port) specified with -L cannot be setup.
            the TAP mirror thread encounters an error reading from or writing to the VPN adapter.
        New INI file directive ExitLevel = 1 that does the same as -x1
    2016-12-12 (1107)
        Fixed a bug in all Cygwin builds that vlmcsd could not be properly stopped if it was started as a service.
        Updated ./src/GNUmakefile to include CFLAG NO_TAP in FEATURES=minimum
        Updated GNUmakefile help to explain CFLAG NO_TAP
        Fixed a bug in all Windows and Cygwin builds with TCP port locking
        Worked around a problem with POSIX 2008 compatibility in the bionic library of Android 1.5 builds that realpath is unable to allocate a string buffer.
    2016-12-06 (1106)
        Windows and Cygwin versions of vlmcsd have new command line option -O to use an OpenVPN Tap or TeamViewer VPN adapter for easy self-activation
        New INI file directive VPN= (same as command line option -O)
        New CFLAG NO_TAP that compiles vlmcsd without support for a TAP or TeamViewer VPN adapter.
        Fixed a bug that time spans in command line options -O, -A and -R were misinterpreted in rare cases.


Source from [http://forums.mydigitallife.info/threads/50234](http://forums.mydigitallife.info/threads/50234)
