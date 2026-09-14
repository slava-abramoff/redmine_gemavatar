# Gemavatar (Redmine 6+)

## Disclaimer
This is a fork made for a fork that forked a fork which adapts this plugin for Redmine 6. **This fork fixes the issue with avatar styles**.

## About
``Gemavatar`` is a ``Redmine`` plugin for replacing the gravatars (they must 
be enabled) with the jpeg pictures stored in the ldap auth_source that 
``Redmine`` is configured to work with.

Installation
------------

Git clone the repo in the plugins folder
`git clone https://github.com/slava-abramoff/redmine_gemavatar.git`

Please be sure that the folder is named `redmine_gemavatar`

Do the migration on the database (will create the table with the pictures):

`ruby bin/rake redmine:plugins RAILS_ENV="production"`

Restart the web server service.

Configuration
-------------

Go to Administration -> Plugins and click ``Configure`` on the Gemavatar
plugin.

There you must set:

- The maximum time the avatars are cached on disk.
- Whether to allow users to refetch their own avatar from AD.
- The string that defines the property in your LDAP server where the photo is stored (`thumbnailphoto` works for me, but `jpegphoto` was the original plugin value)


