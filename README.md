# TeamCal Neo 4 Beta

Please note, that TeamCal Neo 4 is a new major release and is not compatible with previous versions of TeamCal Neo. 
However, you can upgrade your existing TeamCal Neo 3 installation to TeamCal Neo 4 by following the instructions in the
upgrade guide below.

## Changes in the new release
TeamCal Neo 4 comes with several updates and improvements. Also, some features have been removed since they were not
state of the art anymore. Here are some of the most important changes:

### Bugfixes
- Fixed Bootstrap 5 class bugs
- Fixed missing user in sample SQL
- [Fixed reset password on users page](https://github.com/glewe/teamcal-neo/issues/5)

### New Features
- Added content narrow and wide mode toggle
- Vertical sidebar menu for wide screens
- [Absence patterns](https://lewe.gitbook.io/teamcal-neo/administration/absence-patterns)
- [Added LDAP test configuration](https://github.com/glewe/teamcal-neo/issues/3)
- [Added Bootstrap Dark and Light mode](https://github.com/glewe/teamcal-neo/issues/2)
- Added Bootstrap Icons

### Improvements
- New TeamCal Neo icon
- Faster permission check
- Cleaner form and page layout
- Footer links were reduced to Data Privacy and Imprint (smaller footer)
- Database optimizations
- [Added client IP address to log entries](https://github.com/glewe/teamcal-neo/issues/4)
- [Added autoclose option to alert messages](https://github.com/glewe/teamcal-neo/issues/1)
- Nicer release information on the About page

### Removed Features
- Removed Banner option (outdated feature)
- Removed Bootswatch user themes (partially incompatible, unnecessary maintenance)
- Removed X-editable addon (unused)
- Removed Select2 addon (unused)
- Removed google-code-prettify addon (unused)
- Removed TeamCal Pro import feature (use 3.9.3 first if you still need it)

## Upgrade Guide
To upgrade your existing TeamCal Neo 3 installation to TeamCal Neo 4, please follow these steps:
1. Backup your existing TeamCal Neo 3 installation
2. Delete the following folders:
    - /addons/google-code-prettify
    - /addons/select2
    - /addons/x-editable
    - /themes/(all folders but 'bootstrap')
    - /images/icons/logo-*.png
3. Download the new release, unzip and overwrite all files
4. Changes in your database: Run the SQL statements from the file:
    - /sql/upgrade_3.9.3_to_4.0.0.sql
5. Edit config/config.app.php and change line 39 to:
   `define('APP_INSTALLED',"1");`
6. Edit config/config.db.php and update your database settings from your backup.
7. Delete file installation.php in the root directory.

## Feedback
I'd love to read your feedback or questions. Pllease feel free to open an issue on GitHub.

[TeamCal Neo issues](https://github.com/glewe/teamcal-neo/issues)

Best regards,
George Lewe

