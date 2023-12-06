# Install apache2 in ubuntu

Installing apache2 on ubuntu Installing from source

```
Installing from source
Download	Download the latest release from http://httpd.apache.org/download.cgi
Extract	$ gzip -d httpd-NN.tar.gz
$ tar xvf httpd-NN.tar
$ cd httpd-NN
Configure	$ ./configure --prefix=PREFIX
Compile	$ make
Install	$ make install
Customize	$ vi PREFIX/conf/httpd.conf
Test	$ PREFIX/bin/apachectl -k start
```

Sometime during make you might face an error [configure: error: APR not found](https://stackoverflow.com/questions/13967114/configure-error-apr-not-found-please-read-the-documentation). Simple solution is to wget **aprXX** and **apr-utilXX** from [http://apr.apache.org/download.cgi](http://apr.apache.org/download.cgi) and extract it to _srclib_ and rename it to **apr** and **apr-util** respectively.

aftre this edit _conf/httpd.conf_ and add&#x20;

```
ServerName localhost

<Directory />
    Options FollowSymLinks
    AllowOverride All
    Order deny,allow
    Allow from all
</Directory>
```

apache2 server will be setup on localhost:80.



Now , how to set up an alias to a file/folder. Add below lines in same same conf file

```
Alias /webfiles "/scratch/hra/apache2/webfiles"
<Directory "/scratch/hra/apache2/webfiles">
    Options Indexes FollowSymLinks
    AllowOverride None
    Require all granted
</Directory>

```

With this you can access a file placed in _/webfiles_ folder using _localhost:80/webfiles/test.txt_
