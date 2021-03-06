# Free Company Lodestone Fetcher by Jack Wallace (Malrik Rohan @ Leviathan)
Live demo @ www.legionofhalone.com/roster

**viion's XIVPads-LodestoneAPI used for parsing Lodestone (for license info and more see https://github.com/viion/XIVPads-LodestoneAPI).**


## Requirements

- PHP 5.4+
- MySQL 5 with MySQLi support
- Web server/provider with support for 20~30+ Mb of script memory usage (depending on FC size)
- CURL enabled on your server

## Install

- Install the database schema using the provided schema.sql file.
- Add database information to config.php file along with Free Company information (see comments in config.php).
- Upload files to web server.
- Setup a cron job for cron.php. I'd suggest renaming this so people can't go to your site and simply look for cron.php and execute it over and over. More in notes below.
- Include roster.php into whatever page you require!

## Notes

- I use the Wordpress plugin "Allow PHP in Posts and Pages" to import this into a Wordpress site, with this you can simply write [php]include 'roster.php';[/php] into a page or post. If you upload the files into the root of your Wordpress install, the roster will appear.
- The appearance of the table is controlled entirely by style.css. All changes to the table in regards to image size, etc, are done through this.
- If you want to enable debug messages, change the "$debug = false;" line in config.php to true. This will output information that is useful to troubleshoot what's going on/wrong.
- If you want to output to a log instead, view the top function in functions.php. The default simply prints debug messages on runtime, whereas log will do it whenever anyone views it. WARNING : log sizes can become large very quickly if you enable the option to output to file and forget about it!

**License**
- MIT License : Copyright (c) 2014 Jack Wallace
- You may: use, redistribute, modify, share, collaborate, change spaces to tabs, so long as the comment license stays intack at the top. IF YOU MAKE MODIFICATIONS please add your contribution details (name/git handle) in the readme.