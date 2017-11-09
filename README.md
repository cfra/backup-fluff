# backup-fluff

<aside class="warning">
Highly experimental. No restore.
</aside>

## Concept

Trying to restore and backup in line with [RFC1925](https://tools.ietf.org/html/rfc1925)
Especially trying to avoid [this](https://xkcd.com/1360/) and also [that](https://xkcd.com/1718/)

backup-fluff is based on the concept of a job.

## Job

A job is defined by its name.

Sane defaults are derived from that name.

They can be overwritten with config.

A job has different tasks.

### Backup

Backups are tracked in a zfs dataset.

Each successful backup creates a snapshot.

Data to be backed up is transferred with [rsync](https://arstechnica.com/information-technology/2015/12/rsync-net-zfs-replication-to-the-cloud-is-finally-here-and-its-fast/).

