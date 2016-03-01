SSH remotes without default ports
=================================

It is not always possible to use SSH's default port and this brings some
complications when git remotes are involved. Unfortunately the common
'url:port' syntax does not seem to work. SSH's config file may be used to work
around this problem:

    Host github
        HostName github.com
        Port 22
        User git

Now you can clone a project like this:

    git clone github:herberthamaral/til.git


References:
[1] - http://stackoverflow.com/questions/1558719/using-a-remote-repository-with-non-standard-port
[2] - http://nerderati.com/2011/03/17/simplify-your-life-with-an-ssh-config-file/
