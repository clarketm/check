# check
Check if a TCP/UDP port is open on a host(s) using UNIX command line tools.

### Usage
```bash
$ check --help

NAME:
	 check – check if a TCP/UDP port is open on a host(s).


SYNOPSIS:
	 check [ opts... ] hostname...


OPTIONS:
	 -h, --help                             	 Print options and usage information.
	 -n, --noexit                           	 Continue processing hostnames on failure.
	 -p, --port port       	 Port number (default: 80).
	 -s, --silent                           	 Suppress terminal output.
	 -t, --timeout seconds 	 Timeout for the connection (default: 5).
	 -v, --version                          	 Print current version number.


EXIT CODE:
	 0    	 SUCCESS: Port is open on the specified host.
	 1    	 FAILURE: Port is closed on the specified host.
	 2    	 ERROR: Option parsing error.
	 3    	 ERROR: Option argument missing.
	 4    	 ERROR: Invalid option argument.
	 5    	 ERROR: GNU getopt not found on PATH.
	 6    	 ERROR: General or unknown error.


EXAMPLES:
	 check "www.travismclarke.com" "www.google.com" --port 443 --timeout 3
```

### Example
```bash
$ check "www.travismclarke.com" "www.google.com" --port 443 --timeout 3 ; echo "exit_code: $?"

# output
www.travismclarke.com: success
www.google.com: success
exit_code: 0
```
