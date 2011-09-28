# resolve #

About
--------

License: [GNU General Public License v3][1]

Resolve is an, open-source wrapper to the host command.

If you need to resolve process multiple IP addresses to host names then resolve should be able to help you. IP address can be piped into resolve. In addition resolve will attempt to resolve any command line arguments.

Please keep in mind that if you are running Apache, that there is an option called "HostnameLookups" which you may wish to enable or disable depending upon your requirements.

If you wish to monitor log files which are periodically rotated then the perl module [FileTail][2] may be of interest.

Resolve is open source, therefore if you make improvements please fork and submit a pull request.

Clone the repo and and resolve your IP addresses.

Usage Examples
---------

Below is an eample of how to use resolve : 
cat /var/log/httpd/access_log | awk '{print $1}' | sort -u | /path/to/reslove

This will provide a list of IP address and the domain names of machines who have been accessing your apache web server. This means you will not need to configure Apache to resolve DNS names in the logs.

There are various other ways you may find to use resolve.

If you have any questions, comments or suggestions please make contact.

Known issues
---------

When using the -f option and the --apachetime option the last time available in the logs for that particular IP address (if available) will be reported rather than the time for the particular entry in the log.


Additional Information
---------
Check the [wiki][3] for further examples of how to use resolve.

  [1]: http://www.gnu.org/licenses/gpl.html
  [2]: href="http://search.cpan.org/~mgrabnar/File-Tail-0.99.3/Tail.pm">FileTail
  [3]:https://github.com/henri/resolve/wiki
