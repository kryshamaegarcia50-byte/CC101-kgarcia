# Backup Script Guide

## 1. What Is a Backup?
A backup is a copy of important files that can be restored if the original files are lost, damaged, or accidentally deleted.

## 2. Purpose of the Backup Script
The backup script automatically creates a compressed copy of the client's application data. It saves time and helps protect important information.

## 3. Bash Backup Script
The following script creates a timestamped backup of the app-data folder.

    #!/bin/bash
    # Automated Backup Script for CloudNova Technologies

    SOURCE_DIR="app-data"
    BACKUP_DIR="backups"
    TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

    echo "Initiating automated backup..."

    mkdir -p "$BACKUP_DIR"

    tar -czf "$BACKUP_DIR/backup_$TIMESTAMP.tar.gz" "$SOURCE_DIR"

    echo "Backup completed successfully at $TIMESTAMP!"

## 4. Explanation of the Commands
- `#!/bin/bash` tells Linux to use Bash to execute the script.
- `SOURCE_DIR` stores the name of the folder containing the client data.
- `BACKUP_DIR` specifies where the backup files will be saved.
- `TIMESTAMP` adds the current date and time to the backup filename.
- `mkdir -p` creates the backup directory if it does not exist.
- `tar -czf` creates a compressed `.tar.gz` archive.
- `echo` displays messages in the terminal.

## 5. Test Data
The sample file is `app-data/data.txt`. Its content is:

    This is critical client data.

This represents important client information that needs protection.

## 6. Verify the Backup
To list the backup archives, run:

    ls -lh backups/

To inspect a specific archive, run:

    tar -tzf backups/backup_YYYYMMDD_HHMMSS.tar.gz

Replace the example filename with an actual backup filename. The archive should contain `app-data/` and `app-data/data.txt`.

## 7. Cron Job Scheduling
A cron job can run the backup script automatically every day at 2:00 AM.

    0 2 * * * /root/CC101-kgarcia/Laboratory-09-Cloud-Automation-Engineer/backup.sh

The computer must be running and the cron service must be active for the scheduled task to execute.

## 8. Conclusion
Backup automation helps cloud engineers save time and protect important data. Backup files should be verified regularly, stored securely, and tested to ensure that they can be restored.
