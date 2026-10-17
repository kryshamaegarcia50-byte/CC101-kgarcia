# Backup Script Guide

## 1. Purpose of the Backup Script

The backup script automates the process of creating a compressed backup of the client's application data. It saves time, reduces repetitive manual work, and helps protect important files from accidental loss.

## 2. Full Backup Script

The following is the complete Bash script used in this laboratory.

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p "$BACKUP_DIR"

# Compress the source directory into a tarball (.tar.gz)
tar -czf "$BACKUP_DIR/backup_$TIMESTAMP.tar.gz" "$SOURCE_DIR"

echo "Backup completed successfully at $TIMESTAMP!"
```

## 3. Explanation of the Script

- `#!/bin/bash` tells the operating system to use Bash to execute the script.
- `SOURCE_DIR="app-data"` defines the folder containing the client's data.
- `BACKUP_DIR="backups"` defines where the backup archives will be stored.
- `TIMESTAMP=$(date +"%Y%m%d_%H%M%S")` generates a timestamp for each backup filename.
- `echo` displays messages in the terminal.
- `mkdir -p "$BACKUP_DIR"` creates the backup directory if it does not already exist.
- `tar -czf` creates a compressed `.tar.gz` archive containing the source directory.

## 4. File Permissions: chmod +x

The command `chmod +x backup.sh` adds execute permission to the backup script. This allows the user to run the script directly with `./backup.sh` instead of receiving a permission-denied error, provided the user also has the necessary access to the file and its directory.

## 5. Cron Job Schedule

The cron expression used for this laboratory is:

```cron
0 2 * * * /root/CC101-kgarcia/Laboratory-09-Cloud-Automation-Engineer/backup.sh
```

This schedules the backup script to run every day at 2:00 AM, using the full path to the script in the KillerCoda environment.

### Breakdown of the Five Time Fields

| Field | Value | Meaning |
|---|---|---|
| Minute | `0` | Runs at minute zero. |
| Hour | `2` | Runs at 2 AM. |
| Day of Month | `*` | Runs every day of the month. |
| Month | `*` | Runs every month. |
| Day of Week | `*` | Runs every day of the week. |

The five fields determine when the scheduled command runs. The command after those fields identifies the script to execute.

## 6. Testing and Verification

The following commands were used to create, run, and verify the backup:

```bash
mkdir -p app-data
echo "This is critical client data." > app-data/data.txt
chmod +x backup.sh
./backup.sh
ls -lh backups/
tar -tzf backups/backup_20261017_051806.tar.gz
crontab -l
```

The archive listing should contain `app-data/` and `app-data/data.txt`. The timestamped archive filename may differ depending on when the script runs.

## 7. Conclusion

Bash scripting and cron scheduling help cloud engineers automate routine backup operations. The executable permission allows the script to run directly, while cron can schedule it to execute automatically. Backup archives should be verified regularly, stored securely, and tested for successful restoration.
