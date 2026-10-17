# Laboratory 09: Cloud Automation Engineer

## Mission Overview

This laboratory introduces cloud automation through Bash scripting and scheduled backup operations. The project simulates a simple client data backup process for CloudNova Technologies using Linux commands, compressed archives, and cron scheduling.

## Objectives

- Understand the fundamentals of cloud automation.
- Research Bash scripts, variables, and cron jobs.
- Create sample client data for backup testing.
- Write and execute a Bash backup script.
- Apply executable permissions using `chmod +x`.
- Create and verify compressed `.tar.gz` backup files.
- Configure a cron job to schedule automatic backups.
- Document the process and maintain the project using Git and GitHub.

## Commands Executed

| Command | Purpose |
|---|---|
| `git clone` | Downloads the GitHub repository to the playground. |
| `mkdir -p app-data` | Creates the directory for sample client data. |
| `echo "This is critical client data." > app-data/data.txt` | Creates a test file containing sample data. |
| `nano backup.sh` | Opens the Nano editor to create or edit the script. |
| `chmod +x backup.sh` | Grants execute permission to the script. |
| `./backup.sh` | Runs the backup script. |
| `mkdir -p backups` | Creates the backup destination directory if needed. |
| `ls -lh backups/` | Lists backup archives and their file sizes. |
| `tar -tzf ARCHIVE.tar.gz` | Lists the contents of a specified compressed archive. |
| `crontab -l` | Displays the current user's scheduled cron jobs. |
| `env EDITOR=nano crontab -e` | Opens the cron table in Nano for editing. |
| `git add` | Stages project files for version control. |
| `git commit` | Saves a checkpoint in the local Git history. |
| `git push origin main` | Pushes committed changes to GitHub. |

## Skills Learned

- Writing basic Bash automation scripts.
- Using variables to manage directories and filenames.
- Creating compressed backups with `tar`.
- Managing file permissions in Linux.
- Scheduling recurring tasks with cron.
- Verifying backup files and their contents.
- Documenting technical procedures.
- Using Git and GitHub to track and publish project changes.

## Project Structure

- `README.md` - Project overview, objectives, commands, and skills learned.
- `automation-research.md` - Research on Bash scripts, variables, and cron jobs.
- `backup-script-guide.md` - Backup script, permissions, cron schedule, and technical documentation.
- `backup.sh` - Bash script that creates compressed backups.
- `app-data/` - Sample client data.
- `backups/` - Generated backup archives.
- `screenshots/` - Evidence of completed laboratory tasks.

## Conclusion

This laboratory demonstrates how simple Linux tools can automate routine backup operations. The script creates timestamped compressed archives, while cron can schedule recurring execution. Reliable backup practices also require verification, secure storage, and testing restoration procedures.
