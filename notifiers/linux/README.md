Linux notifier for CSS Live Reload
==================================

Install
-------

This notifier is written in Perl. To install it, you need to have perl installed in your system, as well as the following CPAN packages:
```
Net::WebSocket::Server
File::Find
Linux::Inotify2
AnyEvent
```
CPAN packages are installed like this:
```shell
perl -MCPAN -e 'install Net::WebSocket::Server'
perl -MCPAN -e 'install File::Find'
perl -MCPAN -e 'install Linux::Inotify2'
perl -MCPAN -e 'install AnyEvent'
```
Then, download the CLR notifier script to your `/usr/local/bin` directory:
```
cd /usr/local/bin 
sudo wget https://raw.github.com/sergiosgc/CSS-Live-Reloader/master/notifiers/linux/clr-notifier
sudo chmod a+x clr-notifier
```

Usage
-----

To use, just `cd` to the directory containing your project's CSS files and run the notifier:
```shell
cd .../my_project_dir/css
clr-notifier
```

Then, visit the page that uses the CSS and press F9. The extension will reload the CSS and establish a connection to the notification server. Now, edit away your CSS files. The page will refresh automatically!
