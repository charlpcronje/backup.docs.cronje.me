```sh
 __ .__..  ..___._..__    .__ .__. __ .  ..  ..__  __.   .  ..___
/  `|  ||\ |[__  | [ __   [__)[__]/  `|_/ |  |[__)(__    |\/|[__ 
\__.|__|| \||   _|_[_./ * [__)|  |\__.|  \|__||   .__) * |  |[___
                                                                 
```

- This repo will become a sub-module of docs.devserv.me.
- Go to [./src/README.md](./src/README.md) for the root of this repo

=== Synopsis
- Okay so for now I want to start editing some config files, but I want to keep history of my configs, so I'm going to investigate the best way to achieve this. I just don't want to keep on creating config.bak or .old or .thisIsLame.

- So what I decided, I'm not sure how scaleable this will be, but I'm going to create GIT repo in /etc. Every file I edit I will `git add [filename]` and after every config update I will do a commit.

- So 1st I have to [install GIT](http://setup.docs.devserv.me/git)

- But I decided I want to automate this in a way. I usually use nano to quickly edit a config file. So what would be cool is if I created a new command... Something called `edit` that will be used instead of calling `nano` direcrt

- In the end I called it `edit` because some people like VI others prefer Nano I added a feature that you can enter the following command to set your defaut text edit
===
