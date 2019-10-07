# nmap-cve2019-15846

Exim before 4.92.2 allows remote attackers to execute arbitrary code
as root via a trailing backslash. The vulnerability is exploitable
by sending a SNI ending in a backslash-null sequence during the initial
TLS handshake. The exploit exists as a POC.
For more details see doc/doc-txt/cve-2019-15846/ in the source code
repository.

Reference:

* http://exim.org/static/doc/security/CVE-2019-15846.txt
* http://lists.opensuse.org/opensuse-security-announce/2019-09/msg00024.html
* http://www.openwall.com/lists/oss-security/2019/09/06/2
* http://www.openwall.com/lists/oss-security/2019/09/06/4
* http://www.openwall.com/lists/oss-security/2019/09/06/5

# Usage 

`nmap --script=smtp-vuln-cve2019-15846 -pT:25,465,587 <host>`

# Installation

1. Git clone this repository
2. `cd nmap-cve2019-15846`
3. `mv smtp-vuln-cve2019-15846.nse /usr/share/nmap/scripts`
