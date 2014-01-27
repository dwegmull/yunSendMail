yunSendMail
===========

A simple Arduino Yun sketch and Linux side send mail configuration. It sends an email each time the Atmel processor boots.

In order to use it, you need to install a small mail program on the Linux part of the Yun.
Connect to the Yun via ssh:
root@Arduino:/# opkg update
root@Arduino:/# opkg install ssmtp
Now you need to configure it. Installation created the following file: /etc/ssmtp/ssmtp.conf
Edit it to match the custom one from the git repository (obviously, you need to use your own Email setup).
root@Arduino:/# vi /etc/ssmtp/ssmtp.conf
You can close the ssh connection.
Now open the sketch in Arduino 1.5.5 or newer. 
Set your to and from email addresses on the line that starts with script.print("echo
Upload it and a few seconds (or minutes depending on your mail server), you will get an Email!
The email will be sent everytime the Atmel processor is rebooted. 
