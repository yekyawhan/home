---
{"dg-publish":true,"permalink":"/everything-about-linux/crontab-schedule/","dgPassFrontmatter":true,"noteIcon":""}
---

(https://www.geeksforgeeks.org/crontab-in-linux-with-examples/)
crontab -e
crontab -l

Keyword    Equivalent
@yearly    0 0 1 1 *
@daily     0 0 * * *
@hourly    0 * * * *
@reboot    Run at startup.
	

@reboot [path to command] [argument1] [argument2] … [argument n] 
@reboot [part to shell script]


sudo systemctl status cron.service
sudo systemctl enable cron.service

## Run a Cron Job at Boot With Delay

```
To run a job with a delay after the system reboots, use the [sleep command](https://phoenixnap.com/kb/linux-sleep) when adding the **`@reboot`** string:

```
@reboot sleep [time in seconds] && [path to job]
```

If you want to create a text file with the system date five minutes after reboot, add:

```
@reboot sleep 300 && date >> ~/date.txt
## Remove a Reboot Command

Each **`@reboot`** string you add to the cron task list runs a job every time Linux restarts. If you no longer wish to run a job, remove it from the task list.

To do this, open the task list using the **`crontab -e`** command. Scroll down to the bottom to review the jobs you added.

To remove a task from the list, delete the appropriate line from the appropriate string. Press **`Control + X`** to exit Nano, then **`Y`** and **`Enter`** to save changes.




```ad-tip
title: what is different between 'crontab -e' and 'nano /etc/crontab'
collapse: open

The main difference between `crontab -e` and `nano /etc/crontab` lies in how they are used to edit the crontab file.

1. `crontab -e`: This command is used to edit the crontab file for the current user. When you run `crontab -e`, it opens the crontab file associated with your user account in the default text editor (usually set in the `EDITOR` environment variable, which defaults to `vi` or `nano`).
    
    This method is recommended for editing the crontab file because it ensures that you're modifying the correct crontab for your user. Each user on the system can have their own crontab file, and `crontab -e` edits the crontab specific to the user who executes the command.
    
2. `nano /etc/crontab`: This command is used to directly edit the system-wide crontab file located at `/etc/crontab`. When you run `nano /etc/crontab`, you're editing the crontab file that applies to all users on the system.
    
    Directly editing `/etc/crontab` is less common and generally not recommended unless you have specific system-wide tasks that need to be managed by the root user. It's preferable to use `crontab -e` for user-specific cron jobs and maintain system-wide tasks in separate cron files within the `/etc/cron.d/` directory.
    

In summary, `crontab -e` is used to edit the user-specific crontab file, while `nano /etc/crontab` is used to edit the system-wide crontab file.
```

