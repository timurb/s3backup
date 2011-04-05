# General info

A script to backup stuff to S3

It requires s3sync gem installed.


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
