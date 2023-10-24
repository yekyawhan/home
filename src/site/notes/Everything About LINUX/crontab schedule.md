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
	
	![[Pasted image 20230826004501.png\|Pasted image 20230826004501.png]]


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


Y3KH SETTING

	@reboot /bin/sh ~/home/y3kh/Desktop/audiotransfer.sh
	