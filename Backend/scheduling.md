# Commands & Scheduling
It's important to setup scheduler in-order to make use of few repetitive task which are automated using Laravel scheduler & command.

### Starting The Scheduler
Almost every Linux distribution has some form of cron installed by default. However, if you’re using an Ubuntu machine on which cron isn’t installed, you can install it using APT.
Before installing cron on an Ubuntu machine,
Update the local package index:
`sudo apt update`

Then install cron with the following command: <br>
`sudo apt install cron` <br>  
`sudo systemctl enable cron`

You can follow along the detailed tutorial at [DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-use-cron-to-automate-tasks-ubuntu-1804)

In you crontab file you'll have to create a cron tab entry with following details: <br>
`* * * * * cd /path-to-your-project && php artisan schedule:run >> /dev/null 2>&1`

### List of commands
At the time of writing, We're making use of two custom commands as following:
1) `tokens:clear` everyThirtyMinutes <br>
    This command invalidates any session that was not used in last 2 hours. It make the application secure against compromised tokens.

2) `notifications:clear` <br>
    This command will clear out notifications, Mainly OTP notification etc.

You can run these two commands using SSH Connection, However these are meant to be called automatically by the scheduler.

### Queue Setup
We're making use of Queue for Email Sending, OTP Generation & Notifications. It'll be required to setup queue driver properly. <br>
You can install supervisor using `sudo apt-get install supervisor` command.

Supervisor configuration files are typically stored in the `/etc/supervisor/conf.d` directory. Within this directory, you may create any number of configuration files that instruct supervisor how your processes should be monitored. For example, Create a `laravel-worker.conf` file that starts and monitors a queue:work process:

```
[program:laravel-worker]
process_name=%(program_name)s_%(process_num)02d
command=php /var/www/app.com/artisan queue:work sqs --sleep=3 --tries=3
autostart=true
autorestart=true
user=ubuntu
numprocs=3
redirect_stderr=true
stdout_logfile=/home/forge/app.com/worker.log
stopwaitsecs=3600
```

