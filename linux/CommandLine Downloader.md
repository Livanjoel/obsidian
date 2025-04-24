wget -- Command line tool for download directs links
#see 
https://www.gnu.org/software/wget/manual/html_node/Wgetrc-Commands.html#Wgetrc-Commands
```
man wget
```

6.3 Wgetrc Commands
The complete set of commands is listed below. Legal values are listed after the ‘=’. Simple Boolean values can be set or unset using ‘on’ and ‘off’ or ‘1’ and ‘0’.

Some commands take pseudo-arbitrary values. address values can be hostnames or dotted-quad IP addresses. n can be any positive integer, or ‘inf’ for infinity, where appropriate. string values can be any non-empty string.

Most of these commands have direct command-line equivalents. Also, any wgetrc command can be specified on the command line using the ‘--execute’ switch (see Basic Startup Options.)

accept/reject = string
Same as ‘-A’/‘-R’ (see Types of Files).

add_hostdir = on/off
Enable/disable host-prefixed file names. ‘-nH’ disables it.

ask_password = on/off
Prompt for a password for each connection established. Cannot be specified when ‘--password’ is being used, because they are mutually exclusive. Equivalent to ‘--ask-password’.

auth_no_challenge = on/off
If this option is given, Wget will send Basic HTTP authentication information (plaintext username and password) for all requests. See ‘--auth-no-challenge’.

background = on/off
Enable/disable going to background—the same as ‘-b’ (which enables it).

backup_converted = on/off
Enable/disable saving pre-converted files with the suffix ‘.orig’—the same as ‘-K’ (which enables it).

backups = number
Use up to number backups for a file. Backups are rotated by adding an incremental counter that starts at ‘1’. The default is ‘0’.

base = string
Consider relative URLs in input files (specified via the ‘input’ command or the ‘--input-file’/‘-i’ option, together with ‘force_html’ or ‘--force-html’) as being relative to string—the same as ‘--base=string’.

bind_address = address
Bind to address, like the ‘--bind-address=address’.

ca_certificate = file
Set the certificate authority bundle file to file. The same as ‘--ca-certificate=file’.

ca_directory = directory
Set the directory used for certificate authorities. The same as ‘--ca-directory=directory’.

cache = on/off
When set to off, disallow server-caching. See the ‘--no-cache’ option.

certificate = file
Set the client certificate file name to file. The same as ‘--certificate=file’.

certificate_type = string
Specify the type of the client certificate, legal values being ‘PEM’ (the default) and ‘DER’ (aka ASN1). The same as ‘--certificate-type=string’.

check_certificate = on/off
If this is set to off, the server certificate is not checked against the specified client authorities. The default is “on”. The same as ‘--check-certificate’.

connect_timeout = n
Set the connect timeout—the same as ‘--connect-timeout’.

content_disposition = on/off
Turn on recognition of the (non-standard) ‘Content-Disposition’ HTTP header—if set to ‘on’, the same as ‘--content-disposition’.

trust_server_names = on/off
If set to on, construct the local file name from redirection URLs rather than original URLs.

continue = on/off
If set to on, force continuation of preexistent partially retrieved files. See ‘-c’ before setting it.

convert_links = on/off
Convert non-relative links locally. The same as ‘-k’.

cookies = on/off
When set to off, disallow cookies. See the ‘--cookies’ option.

cut_dirs = n
Ignore n remote directory components. Equivalent to ‘--cut-dirs=n’.

debug = on/off
Debug mode, same as ‘-d’.

default_page = string
Default page name—the same as ‘--default-page=string’.

delete_after = on/off
Delete after download—the same as ‘--delete-after’.

dir_prefix = string
Top of directory tree—the same as ‘-P string’.

dirstruct = on/off
Turning dirstruct on or off—the same as ‘-x’ or ‘-nd’, respectively.

dns_cache = on/off
Turn DNS caching on/off. Since DNS caching is on by default, this option is normally used to turn it off and is equivalent to ‘--no-dns-cache’.

dns_timeout = n
Set the DNS timeout—the same as ‘--dns-timeout’.

domains = string
Same as ‘-D’ (see Spanning Hosts).

dot_bytes = n
Specify the number of bytes “contained” in a dot, as seen throughout the retrieval (1024 by default). You can postfix the value with ‘k’ or ‘m’, representing kilobytes and megabytes, respectively. With dot settings you can tailor the dot retrieval to suit your needs, or you can use the predefined styles (see Download Options).

dot_spacing = n
Specify the number of dots in a single cluster (10 by default).

dots_in_line = n
Specify the number of dots that will be printed in each line throughout the retrieval (50 by default).

egd_file = file
Use string as the EGD socket file name. The same as ‘--egd-file=file’.

exclude_directories = string
Specify a comma-separated list of directories you wish to exclude from download—the same as ‘-X string’ (see Directory-Based Limits).

exclude_domains = string
Same as ‘--exclude-domains=string’ (see Spanning Hosts).

follow_ftp = on/off
Follow FTP links from HTML documents—the same as ‘--follow-ftp’.

follow_tags = string
Only follow certain HTML tags when doing a recursive retrieval, just like ‘--follow-tags=string’.

force_html = on/off
If set to on, force the input filename to be regarded as an HTML document—the same as ‘-F’.

ftp_password = string
Set your FTP password to string. Without this setting, the password defaults to ‘-wget@’, which is a useful default for anonymous FTP access.

This command used to be named passwd prior to Wget 1.10.

ftp_proxy = string
Use string as FTP proxy, instead of the one specified in environment.

ftp_user = string
Set FTP user to string.

This command used to be named login prior to Wget 1.10.

glob = on/off
Turn globbing on/off—the same as ‘--glob’ and ‘--no-glob’.

header = string
Define a header for HTTP downloads, like using ‘--header=string’.

compression = string
Choose the compression type to be used. Legal values are ‘auto’ (the default), ‘gzip’, and ‘none’. The same as ‘--compression=string’.

adjust_extension = on/off
Add a ‘.html’ extension to ‘text/html’ or ‘application/xhtml+xml’ files that lack one, a ‘.css’ extension to ‘text/css’ files that lack one, and a ‘.br’, ‘.Z’, ‘.zlib’ or ‘.gz’ to compressed files like ‘-E’. Previously named ‘html_extension’ (still acceptable, but deprecated).

http_keep_alive = on/off
Turn the keep-alive feature on or off (defaults to on). Turning it off is equivalent to ‘--no-http-keep-alive’.

http_password = string
Set HTTP password, equivalent to ‘--http-password=string’.

http_proxy = string
Use string as HTTP proxy, instead of the one specified in environment.

http_user = string
Set HTTP user to string, equivalent to ‘--http-user=string’.

https_only = on/off
When in recursive mode, only HTTPS links are followed (defaults to off).

https_proxy = string
Use string as HTTPS proxy, instead of the one specified in environment.

ignore_case = on/off
When set to on, match files and directories case insensitively; the same as ‘--ignore-case’.

ignore_length = on/off
When set to on, ignore Content-Length header; the same as ‘--ignore-length’.

ignore_tags = string
Ignore certain HTML tags when doing a recursive retrieval, like ‘--ignore-tags=string’.

include_directories = string
Specify a comma-separated list of directories you wish to follow when downloading—the same as ‘-I string’.

iri = on/off
When set to on, enable internationalized URI (IRI) support; the same as ‘--iri’.

inet4_only = on/off
Force connecting to IPv4 addresses, off by default. You can put this in the global init file to disable Wget’s attempts to resolve and connect to IPv6 hosts. Available only if Wget was compiled with IPv6 support. The same as ‘--inet4-only’ or ‘-4’.

inet6_only = on/off
Force connecting to IPv6 addresses, off by default. Available only if Wget was compiled with IPv6 support. The same as ‘--inet6-only’ or ‘-6’.

input = file
Read the URLs from string, like ‘-i file’.

keep_session_cookies = on/off
When specified, causes ‘save_cookies = on’ to also save session cookies. See ‘--keep-session-cookies’.

limit_rate = rate
Limit the download speed to no more than rate bytes per second. The same as ‘--limit-rate=rate’.

load_cookies = file
Load cookies from file. See ‘--load-cookies file’.

local_encoding = encoding
Force Wget to use encoding as the default system encoding. See ‘--local-encoding’.

logfile = file
Set logfile to file, the same as ‘-o file’.

max_redirect = number
Specifies the maximum number of redirections to follow for a resource. See ‘--max-redirect=number’.

mirror = on/off
Turn mirroring on/off. The same as ‘-m’.

netrc = on/off
Turn reading netrc on or off.

no_clobber = on/off
Same as ‘-nc’.

no_parent = on/off
Disallow retrieving outside the directory hierarchy, like ‘--no-parent’ (see Directory-Based Limits).

no_proxy = string
Use string as the comma-separated list of domains to avoid in proxy loading, instead of the one specified in environment.

output_document = file
Set the output filename—the same as ‘-O file’.

page_requisites = on/off
Download all ancillary documents necessary for a single HTML page to display properly—the same as ‘-p’.

passive_ftp = on/off
Change setting of passive FTP, equivalent to the ‘--passive-ftp’ option.

password = string
Specify password string for both FTP and HTTP file retrieval. This command can be overridden using the ‘ftp_password’ and ‘http_password’ command for FTP and HTTP respectively.

post_data = string
Use POST as the method for all HTTP requests and send string in the request body. The same as ‘--post-data=string’.

post_file = file
Use POST as the method for all HTTP requests and send the contents of file in the request body. The same as ‘--post-file=file’.

prefer_family = none/IPv4/IPv6
When given a choice of several addresses, connect to the addresses with specified address family first. The address order returned by DNS is used without change by default. The same as ‘--prefer-family’, which see for a detailed discussion of why this is useful.

private_key = file
Set the private key file to file. The same as ‘--private-key=file’.

private_key_type = string
Specify the type of the private key, legal values being ‘PEM’ (the default) and ‘DER’ (aka ASN1). The same as ‘--private-type=string’.

progress = string
Set the type of the progress indicator. Legal types are ‘dot’ and ‘bar’. Equivalent to ‘--progress=string’.

protocol_directories = on/off
When set, use the protocol name as a directory component of local file names. The same as ‘--protocol-directories’.

proxy_password = string
Set proxy authentication password to string, like ‘--proxy-password=string’.

proxy_user = string
Set proxy authentication user name to string, like ‘--proxy-user=string’.

quiet = on/off
Quiet mode—the same as ‘-q’.

quota = quota
Specify the download quota, which is useful to put in the global wgetrc. When download quota is specified, Wget will stop retrieving after the download sum has become greater than quota. The quota can be specified in bytes (default), kbytes ‘k’ appended) or mbytes (‘m’ appended). Thus ‘quota = 5m’ will set the quota to 5 megabytes. Note that the user’s startup file overrides system settings.

random_file = file
Use file as a source of randomness on systems lacking /dev/random.

random_wait = on/off
Turn random between-request wait times on or off. The same as ‘--random-wait’.

read_timeout = n
Set the read (and write) timeout—the same as ‘--read-timeout=n’.

reclevel = n
Recursion level (depth)—the same as ‘-l n’.

recursive = on/off
Recursive on/off—the same as ‘-r’.

referer = string
Set HTTP ‘Referer:’ header just like ‘--referer=string’. (Note that it was the folks who wrote the HTTP spec who got the spelling of “referrer” wrong.)

relative_only = on/off
Follow only relative links—the same as ‘-L’ (see Relative Links).

remote_encoding = encoding
Force Wget to use encoding as the default remote server encoding. See ‘--remote-encoding’.

remove_listing = on/off
If set to on, remove FTP listings downloaded by Wget. Setting it to off is the same as ‘--no-remove-listing’.

restrict_file_names = unix/windows
Restrict the file names generated by Wget from URLs. See ‘--restrict-file-names’ for a more detailed description.

retr_symlinks = on/off
When set to on, retrieve symbolic links as if they were plain files; the same as ‘--retr-symlinks’.

retry_connrefused = on/off
When set to on, consider “connection refused” a transient error—the same as ‘--retry-connrefused’.

robots = on/off
Specify whether the norobots convention is respected by Wget, “on” by default. This switch controls both the /robots.txt and the ‘nofollow’ aspect of the spec. See Robot Exclusion, for more details about this. Be sure you know what you are doing before turning this off.

save_cookies = file
Save cookies to file. The same as ‘--save-cookies file’.

save_headers = on/off
Same as ‘--save-headers’.

secure_protocol = string
Choose the secure protocol to be used. Legal values are ‘auto’ (the default), ‘SSLv2’, ‘SSLv3’, and ‘TLSv1’. The same as ‘--secure-protocol=string’.

server_response = on/off
Choose whether or not to print the HTTP and FTP server responses—the same as ‘-S’.

show_all_dns_entries = on/off
When a DNS name is resolved, show all the IP addresses, not just the first three.

span_hosts = on/off
Same as ‘-H’.

spider = on/off
Same as ‘--spider’.

strict_comments = on/off
Same as ‘--strict-comments’.

timeout = n
Set all applicable timeout values to n, the same as ‘-T n’.

timestamping = on/off
Turn timestamping on/off. The same as ‘-N’ (see Time-Stamping).

use_server_timestamps = on/off
If set to ‘off’, Wget won’t set the local file’s timestamp by the one on the server (same as ‘--no-use-server-timestamps’).

tries = n
Set number of retries per URL—the same as ‘-t n’.

use_proxy = on/off
When set to off, don’t use proxy even when proxy-related environment variables are set. In that case it is the same as using ‘--no-proxy’.

user = string
Specify username string for both FTP and HTTP file retrieval. This command can be overridden using the ‘ftp_user’ and ‘http_user’ command for FTP and HTTP respectively.

user_agent = string
User agent identification sent to the HTTP Server—the same as ‘--user-agent=string’.

verbose = on/off
Turn verbose on/off—the same as ‘-v’/‘-nv’.

wait = n
Wait n seconds between retrievals—the same as ‘-w n’.

wait_retry = n
Wait up to n seconds between retries of failed retrievals only—the same as ‘--waitretry=n’. Note that this is turned on by default in the global wgetrc.
