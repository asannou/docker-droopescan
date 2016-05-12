# Run

```
$ docker run -it --rm asannou/droopescan

    |
 ___| ___  ___  ___  ___  ___  ___  ___  ___  ___
|   )|   )|   )|   )|   )|___)|___ |    |   )|   )
|__/ |    |__/ |__/ |__/ |__   __/ |__  |__/||  /
                    |
                                         v1.33.7

Example invocations:
  droopescan scan drupal -u URL_HERE
  droopescan scan silverstripe -u URL_HERE

More info:
  droopescan scan --help

Please see the README file for information regarding proxies.

```

```
$ docker run -it --rm asannou/droopescan scan --help
usage: droopescan (sub-commands ...) [options ...] {arguments ...}

cms scanning functionality.

commands:

  drupal
    drupal related scanning tools

  joomla
    joomla related scanning tools

  silverstripe
    silverstripe related scanning tools

  wordpress
    wordpress related scanning tools

optional arguments:
  -h, --help            show this help message and exit
  --debug               toggle debug output
  --quiet               suppress all output
  -u URL, --url URL
  -U URL_FILE, --url-file URL_FILE
                        A file which contains a list of URLs.
  --enumerate {a,t,i,v,p}, -e {a,t,i,v,p}
                        What to enumerate; default is all available, options are:
                            p - plugins
                            t - themes
                            v - version
                            i - interesting urls
                            a - all
  --method {forbidden,not_found,ok}
                        Some webservers respond with 403 when a folder exists. Others with a 404.
                        Others with a 200; default is to determine.
  --verb {head,get}     The HTTP verb to use; the default option is head,
                        except for version enumeration requests, which are
                        always get because we need to get the hash from the
                        file's contents
  --number NUMBER, -n NUMBER
                        Number of words to attempt from the plugin/theme
                        dictionary. Default is 1000. Use -n 'all' to use all
                        available.
  --plugins-base-url PLUGINS_BASE_URL
                        Location where the plugins are stored by the CMS.
                        Default is the CMS' default location. First %s in
                        string will be replaced with the url, and the second
                        one will be replaced with the module name. E.g.
                        '%ssites/all/modules/%s/'
  --themes-base-url THEMES_BASE_URL
                        Same as above, but for themes.
  --timeout TIMEOUT     How long to wait for an HTTP response before timing
                        out (in seconds).
  --timeout-host TIMEOUT_HOST
                        Maximum time to spend per host (in seconds).
  --no-follow-redirects
                        Prevent the following of redirects.
  --host HOST           Override host header with this value.
  --massscan-override   Overrides defaults with defaults convenient for mass-
                        scanning of hosts.
  --threads THREADS, -t THREADS
                        Number of threads. Default 4.
  --threads-identify THREADS_IDENTIFY
                        Number of threads used for CMS identification.
  --threads-scan THREADS_SCAN
                        Threads used for mass scanning.
  --threads-enumerate THREADS_ENUMERATE
                        Threads used for plugin enumeration.
  --output {json,standard}, -o {json,standard}
                        Output format
  --debug-requests      Prints every HTTP request made and the response
                        returned from the server for debugging purposes.
                        Disables threading and loading bars.
  --error-log ERROR_LOG
                        A file to store the errors on.
  --resume              Resume the url_file scan as of the last known scanned
                        url. Must be used in conjunction with --error-log.

Example invocations:
  droopescan scan drupal -u URL_HERE
  droopescan scan silverstripe -u URL_HERE

More info:
  droopescan scan --help

Please see the README file for information regarding proxies.
```
