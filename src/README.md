---
title: Server Config Backups
---
```sh
 __ .__..  ..___._..__    .__ .__. __ .  ..  ..__  __.   .  ..___
/  `|  ||\ |[__  | [ __   [__)[__]/  `|_/ |  |[__)(__    |\/|[__ 
\__.|__|| \||   _|_[_./ * [__)|  |\__.|  \|__||   .__) * |  |[___
                                                                 
```
## Synopsis

- Okay so for now I want to start editing some config files, but I want to keep history of my configs, so I'm going to investigate the best way to achieve this. I just don't want to keep on creating config.bak or .old or .thisIsLame.

- So what I decided, I'm not sure how scalable this will be, but I'm going to create GIT repo in /etc. Every file I edit I will `git add [filename]` and after every config update I will do a commit.

- So 1st I have to [install GIT](http://setup.docs.CRONje.ME/git)

- But I decided I want to automate this in a way. I usually use nano to quickly edit a config file. So what would be cool is if I created a new command... Something called `edit` that will be used instead of calling `nano` direct

- In the end I called it `edit` because some people like VI others prefer Nano I added a feature that you can enter the following command to set your default text edit


```sh
edit --set-editor
```

## edit httpd.conf

1. Add and commit the file as it is now.
1. Open the file in `nano` and let me make changes
1. When the file closed I should be prompted to describe what I changed
1. That description then gets committed as the commit message to git with the new file again gets pushed to the Private Github repo.
1. I can do this in `Perl`, `Python`, `bash`, `php`, `node` and for that matter `C++`, `Deno` or `Go`. But Ill choose something that I know will be installed anyway so to not bloat the server. So either Node, Python, Perl, or PHP. Php can have some strange issues with shell exec scripts, I'm not sure if Node can run as Sudo without the user being sudo. The quickest will be Bash script, just to prove the concept to myself first.

I'll document this in a new doc...

[Automated GIT Config Backups](configBackups/README.md)
