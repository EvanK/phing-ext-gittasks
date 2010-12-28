# What?

Additional **git** related tasks for the [phing](http://phing.info/) build tool.

# Why?

Phing currently comes with several tasks for interacting with **git** repositories, but it also lacks some that I have a need for.  Thus, I am implementing them myself by extending phing's provided `GitBaseTask` class.  I've implemented them more or less, and [have submitted them to the phing maintainers](http://phing.info/trac/ticket/618) for inclusion in a future release.

# How?

Installing these extra tasks is fairly straightforward, but first you need to locate your phing installation.  In my case, I installed phing via **pear**, which was installed as part of **Zend Server CE**; my phing installation is therefore located in `/usr/local/zend/share/pear/phing`.  Simply copy the `Git*Task.php` files from this repository into `$PHING/tasks/ext/git/` and define them in your build.xml file as *taskdef* entries (similar to what is done in this repo).