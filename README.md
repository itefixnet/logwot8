# Logwot8 - Logrotate for Windows

Logwot8 is a Logrotate implementation for Windows systems. It is a packaging of Logrotate, Cygwin and a collection of related tools to make it a standalone log rotation solution for Windows systems.

## About

The [logrotate](https://github.com/logrotate/logrotate) utility is designed to simplify the administration of log files on a system which generates a lot of log files. Logrotate allows for the automatic rotation, compression, removal and mailing of log files. Logrotate can be set to handle a log file daily, weekly, monthly or when the log file gets to a certain size. Normally, Logrotate is run as a daily scheduled job.

[Cygwin](http://www.cygwin.com/) is a Linux-like environment for Windows. It consists of a DLL (cygwin1.dll), which emulates substantial Linux API functionality, and a collection of tools.

## Features

- **Automatic Log Rotation**: Rotate logs based on size, time, or custom criteria
- **Compression**: Automatically compress rotated logs to save disk space
- **Flexible Scheduling**: Daily, weekly, monthly, or size-based rotation
- **Log Removal**: Automatically remove old log files based on retention policies
- **Windows Integration**: Standalone package designed specifically for Windows systems
- **Cygwin-based**: Leverages Cygwin for Linux-like functionality on Windows

## Use Cases

Logwot8 is ideal for:
- Windows servers generating large amounts of log data
- Applications that don't include native log rotation
- Systems requiring automated log management and retention
- Environments needing consistent log rotation policies across multiple applications

## System Requirements

- **Supported Platforms**: Vista and higher

## Installation

1. Download Logwot8 as a zip file from the [GitHub Releases](https://github.com/itefixnet/logwot8/releases) page
2. Extract the downloaded zip file
3. Run the installer: `logwot8_x.x.x_Installer.exe`
4. Follow the installation wizard:
   - Accept the License agreement
   - Specify an installation location
   - Monitor the installation progress by clicking the 'Details' button for detailed information

## Configuration

After installation, you'll need to configure Logwot8 for your environment:

1. **Edit Configuration File**: Update the configuration file `logwot8.cfg` according to your needs. This file controls which logs to rotate, when to rotate them, and how to handle rotated files.

2. **Configure Email Notifications** (Optional): If you want logrotate to send email notifications, you need to configure the mail functionality:
   - Edit the script `bin/mail`
   - Replace the value of `smtp.server` with your SMTP server address
   - The mail script uses [blat](http://www.blat.net/) for sending emails

3. **Review Configuration Options**: Consult the [online logrotate man page](https://itefix.net/content/logrotate-man-page) for comprehensive configuration options.

## Usage

The batch file `logwot8.cmd` is located at the root of the installation directory. This script starts logrotate in a proper environment.

### Running Manually

```batch
cd C:\Path\To\Logwot8
logwot8.cmd
```

### Scheduling with Task Scheduler

You can use Windows Task Scheduler to run logrotate automatically:

1. Open Windows Task Scheduler
2. Create a new task
3. Set the action to run `logwot8.cmd` from your installation directory
4. Configure the schedule (daily, weekly, monthly, etc.)

## Uninstallation

To remove Logwot8 from your system, simply delete the installation directory.

## Links

- **Website**: [https://itefix.net/logwot8](https://itefix.net/logwot8)
- **GitHub Repository**: [https://github.com/itefixnet/logwot8](https://github.com/itefixnet/logwot8)
- **Releases**: [https://github.com/itefixnet/logwot8/releases](https://github.com/itefixnet/logwot8/releases)
- **Logrotate Man Page**: [https://itefix.net/content/logrotate-man-page](https://itefix.net/content/logrotate-man-page)

## License

Logwot8 is licensed under the BSD 2-Clause License.

