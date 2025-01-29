# Apache2Log

The shell script is a comprehensive Apache log monitoring tool designed for system administrators running Debian-based systems. It utilizes the Linux command-line interface to interact with Apache’s log files, primarily located at /var/log/apache2/access.log, providing a text-based user interface to facilitate log analysis.

Here's what the script includes:

**Main Menu**: The script launches into an interactive main menu, giving users a choice of actions to perform. Each option is clearly outlined, with instructions on how to use the script.

**View Last 100 Log Entries**: Selecting this option displays the most recent 100 entries from the Apache access log. This is useful for a quick check on the latest server activity.

**Interactive Log View**: This option opens the access log file using the less command, allowing users to navigate through the log file interactively. It’s ideal for searching through log entries manually.

**Real-Time Log Monitoring**: Users can choose to view the access log in real time with tail -f, which is crucial for monitoring live server activity, especially when diagnosing issues or tracking active connections.

**Display Last 100 Unique IP Addresses**: This new feature extracts the last 100 unique IP addresses that have made requests to the server. It employs a combination of awk, sort, uniq, and tail to filter and list the addresses, helping identify distinct connections.

**Exit Option**: Allows the user to cleanly exit the script.

The script stands out for its simplicity and ease of use, providing powerful log monitoring capabilities without the need for complex software. It’s particularly suited for quick checks, troubleshooting, and basic log analysis, giving an immediate overview of server health and traffic patterns.

# How to Use

Step : 1 Download
```
git clone https://github.com/byfranke/apache2log
```
Step : 2 Move to directory
```
cd apache2log
```
Step : 3 Permission to execute
```
chmod +x apache2log
```
Step : 4 Run
```
sudo ./apache2log
```

[![Watch the video](https://img.youtube.com/vi/Zy9z5GWk6co/maxresdefault.jpg)](https://www.youtube.com/watch?v=Zy9z5GWk6co)
