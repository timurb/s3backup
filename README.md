# General info

A script to backup stuff to S3

It requires s3sync gem installed.
It does NOT work correctly with python-based or any other s3sync/s3cmd but only with ruby-based one.


# Description

Backups are placed to AWS S3 in a structure like this:

    bucket:/backups/2011-04-05/*
    bucket:/backups/2011-04-06/*
    bucket:/backups/2011-04-07/*

All backups older than 30 days (default) are deleted.

# Configuration

Specify the number of days to keep backups, bucket name and the prefix inside a 
bucket to keep backups in.
The S3 bucket should already be created to run this script.

By default /var/backups and /var/mail are backed up -- change those at the end of file.

# Note

Please note that s3sync utility as stated in its docs does not work with single 
files - only dirs. If you need to backup single file use s3cmd put instead or place
the file into the dir.
