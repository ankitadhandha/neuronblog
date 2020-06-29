---
title: SSL renew
date: "2020-05-20"
tag: "Linux"
---
I have implemented Let's Encrypt SSL in my website, which works fine. 
But it expires every 90 days. I need it to auto renew every 90 days. Is there any easy way to do it?

To update certbot every 3 months, I use `crontab -e` and add following:

    30 07 01 */3 * /path/to/script

    Script will run every 3 months on 1st of month at 07:30 as explained:

    Example of job definition:
    .---------------- minute (0 - 59)
    |  .------------- hour (0 - 23)
    |  |  .---------- day of month (1 - 31)
    |  |  |  .------- month (1 - 12) OR jan,feb,mar,apr ...
    |  |  |  |  .---- day of week (0 - 6) (Sunday=0 or 7) OR sun,mon,tue,wed,thu,fri,sat
    |  |  |  |  |
    *  *  *  *  * user-name command to be executed

My script looks like this:

    `rm -rf /opt/eff.org
    sudo service nginx stop
    sudo /home/ec2-user/certbot-auto --standalone --debug --config /etc/letsencrypt/configs/example.com.conf renew >> /var/log/certbot-renew.log
    sudo service nginx start`

Script should be stored in cron.monthly directory and in executable mode.

This Question is posted on StackOverflow [here](https://stackoverflow.com/questions/62193644/how-to-regularly-update-lets-encrypt-certificate/62193724?noredirect=1) 
Edited by Ankita Bosamiya on 04/06/2020

Click here to [edit](https://github.com/ankitadhandha/zettelkasten/edit/master/45a4ce8cc86c1bfc.md) this file. 

Click here to add [new](https://github.com/ankitadhandha/zettelkasten/new/master) new file.

