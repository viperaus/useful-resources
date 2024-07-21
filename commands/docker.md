# Docker

## Backup and restore data from/to a volume

```
# Define the name of your volume, on macOS/Linux
VOLUME="replace with the name of your volume"
# Define the name of your volume, on Windows (PowerShell)
$VOLUME="replace with the name of your volume"

# Backup:
docker run --rm -v "${VOLUME}:/data" -v "${PWD}:/backup-dir" ubuntu tar cvzf /backup-dir/backup.tar.gz /data
# Restore:
docker run --rm -v "${VOLUME}:/data" -v "${PWD}:/backup-dir" ubuntu bash -c "rm -rf /data/{*,.*}; cd /data && tar xvzf /backup-dir/backup.tar.gz --strip 1"
```
