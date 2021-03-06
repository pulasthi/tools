HBase
======

How to install Apache HBase on Ubuntu 12.04.3
-----------------------------------------------------------
*The following developed documentation is comprised with the guide
of official documentation along with personal encounters with Ubuntu Desktop 12.04.3.*

*Source: http://archanaschangale.wordpress.com/2013/08/29/installing-apache-hbase-on-ubuntu-for-standalone-mode/comment-page-1/*

**First begin by downloading the hbase-0.94.8.tar.gz file using the link above.**

1.	``$ cd Downloads/`` (unzip tar file)
2.	``$ tar –xvf hbase-0.94.8.tar.gz`` (create directory for HBase)
3.	``$ sudo mkdir /usr/lib/hbase-0.94.8`` (move file to HBase directory)
4.	Put in root password, **this may or may not return an error**
  If error returned: type ``$ su`` to enter root password
5.	``$ pwd`` →this will display the directory location

6. Still in downloads? Type ``$ cd ..`` and then Enter →this will change the directory to home

7. Proceed with ``$ pwd`` →now the response should read ``/home/yourusername`` 

8.	``$ mkdir hbase`` →create an HBase directory

9.	``$ cd Downloads`` 

10.	``$ mv hbase-0.94.8 /home/yourusername/hbase`` → HBase will be moved out of the Downloads directory and into the user directory 

11.	``$ cd ..`` →location of file should be confirmed here 

12.	``$ ls –l`` →an organized list of files (white) and directories (blue) will be displayed. HBase should be in **blue** 

13.	``$ ls hbase`` →a file will be displayed in the HBase directory, ``hbase-0.94.8``

**The next steps will concern configuring HBase with Java.**
 If the location of Java Home cannot be recalled, proceed with the following steps:

  ``$ readlink –f $(which java)`` →display will read Java Home location

1.	``$ export JAVA_HOME=/usr/lib/jvm/javahomelocation`` **(drop the /jre/bin/java)** →this step will set the path to the
Java installed in your system 

2.	``$ echo $JAVA_HOME`` →this will confirm the configuration (PLEASE NOTE: ``$`` is used in front of the variable when
referenced, but not when a value is assigned to it) 

The response ought to be what was inserted in step (13) ``/usr/lib/jvm/java-…+``
