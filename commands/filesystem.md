# Useful Filesystem Commands

## List folder sizes

```du -h --max-depth=1```

## List folder sizes - sort by size - include hiden folder (.xxx)

```du -sh .[!.]* *  | sort -h```

## List folder sizes - sort by size - exclude proc and dev folders

```du -h --max-depth=1 --exclude=proc --exclude=dev | sort -h```

## Tar multiple files and delete original

```tar --remove-files -cf 2018-08.tar *2018-08*.log```

## GZip file and remove original

```gzip *2018-08*```

## Create/overwrite file with no contents

```cat /dev/null > logfile```

## Unzip .gz file

```gzip -cdf file.gz > file.txt```

## Import sql file

```mysql -u root -p DATABASENAME < DATABASE.sql```

## List ~ number of connections on port 80

```netstat -an | grep :80 | wc -l```

## Setting file/folder permissions

```
chmod -R 664 ./*
find . -type d -exec chmod 775 {} \;
```
