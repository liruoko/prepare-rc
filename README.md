# prepare-rc.sh

prepare-rc.sh is a simple tool to maintain rc files (such as .vimrc, .zshrc, .screenrc) on many hosts in consistent state


## Suggested workfow

1. store all your actual preferences in a directory ("rc directory"),
2. sync the directory between your hosts using svn, git, Dropbox etc.,
3. to start using preferences from your rc directory, run prepare-rc.sh (once for every of your hosts).

## Structure of rc directory

<pre>
  screenrc/
     screenrc
     screenrc.host.name1
     screenrc.host.name2
     ...
  vimrc/
     vimrc
     vimrc.host.name1
     ...
  zshrc/
     zshrc
  bashrc/
     bashrc
</pre>

## Main features of prepare-rc.sh

* zero dependency -- all you need is /bin/sh
* customizable preferences for different hosts -- useful for predefining windows in .screenrc, or aliases specific for operating system in .zshrc

If you need something more advanced (and aren't afraid of dependencies), 
have a look at rcsync (http://search.cpan.org/~pshangov/App-Rcsync/bin/rcsync), 
it seems to be very powerful and flexible.

