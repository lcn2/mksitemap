# Try mksitemap

Build a sitemap file for a directory of files.


## Install mksitemap

```sh
make install
```

**NOTE**: By default, this installs under `/usr/local/bin/mksitemap`.

Change the `DESTDIR= /usr/local/bin` line in the `Makefile` if needed.


### Example

```sh
$ mksitemap -v 1 /var/www/html http://www.example.com
```


## Run mksitemap

```sh
$ mksitemap topdir site_url
```

Where `topdir` is the top level directory containing your website tree,
and `site_url` is the URL of your site including the leading _http://_ or _https://_.


## To use

```
/usr/local/bin/mksitemap [-h] [-v level] [-V] [-N] topdir site_url

	-h		print help message and exit
	-v level	set verbosity level (def level: 0)
	-V		print version string and exit

	-n		go thru the actions, but do not update any files (def: do the action)
	-N		do not process file, just parse arguments and ignore the file (def: process the file)

	-m maxfiles	maximum number of files in a single sitemap file (def: 35000)

	topdir		set topdir
	site_url	Base URL of the website

Exit codes:
     0         all OK
     2         -h and help string printed or -V and version string printed
     3         command line error
     4         bash version is too old
     5	       some internal tool is not found or not an executable file
     6	       unable to cd or topdir is not a directory
     7	       file under topdir is not a readable file
     8	       unable to determine a method to find the modification time of a file in W3C Datefile format
 >= 10         internal error

mksitemap version: 1.0 2024-06-16
```


# Reporting Security Issues

To report a security issue, please visit "[Reporting Security Issues](https://github.com/lcn2/mksitemap/security/policy)".
