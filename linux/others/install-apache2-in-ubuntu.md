# Install apache2 in ubuntu

Installing apache2 on ubuntu 2Installing from source

| [Download](https://httpd.apache.org/docs/2.4/install.html#download)   | Download the latest release from [http://httpd.apache.org/download.cgi](http://httpd.apache.org/download.cgi#apache24)                                                                                         |
| --------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Extract](https://httpd.apache.org/docs/2.4/install.html#extract)     | <p><code>$ gzip -d httpd-</code><em><code>NN</code></em><code>.tar.gz</code><br><code>$ tar xvf httpd-</code><em><code>NN</code></em><code>.tar</code><br><code>$ cd httpd-</code><em><code>NN</code></em></p> |
| [Configure](https://httpd.apache.org/docs/2.4/install.html#configure) | `$ ./configure --prefix=`_`PREFIX`_                                                                                                                                                                            |
| [Compile](https://httpd.apache.org/docs/2.4/install.html#compile)     | `$ make`                                                                                                                                                                                                       |
| [Install](https://httpd.apache.org/docs/2.4/install.html#install)     | `$ make install`                                                                                                                                                                                               |
| [Customize](https://httpd.apache.org/docs/2.4/install.html#customize) | `$ vi`` `_`PREFIX`_`/conf/httpd.conf`                                                                                                                                                                          |
| [Test](https://httpd.apache.org/docs/2.4/install.html#test)           | <p></p><p><code>$ </code><em><code>PREFIX</code></em><code>/bin/apachectl -k start</code></p>                                                                                                                  |

