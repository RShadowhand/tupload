# Tupload - A tool to upload text to any "fiche" server.

Usage: `tupload <FILE> [OPTIONS] [--server "<ADDRESS> <PORT>"]`  

OPTIONS:

| Short | Long | Function |
|-------|----------|---------------------------------------------------------------|
| -h | --help | Show help message with the copyright. |
| -s | --string | Input is not file. |
| -f | --file | Input is file. (Default) |
| N/A | --server | Change server to "\<ADDRESS\> \<PORT\>". Must be at the end. |
| -n | --noclip | Print the link. If clipboard cannot be used, this is default. |

---
### Important Notes
Tupload will detect your OS and copy the link to your clipboard if possible.  
It supports Cygwin, Linux and OSX, and Bourne shells.  
Tupload **WILL** override your clipboard. Use `-n` if you want to prevent this.  
On Linux, Tupload will attempt to use xclip. If X or xclip isn't installed, it will assume `--noclip` by default.  
The option `--server` **MUST** be at the end of the command, and it **MUST** have address and port. Otherwise it will fail.

---

### Installing

* `wget https://raw.github.com/RShadowhand/tupload/master/tupload`
* `mv ./tupload /usr/bin/tupload` (or any place that's in your PATH. I use ~/bin/ for example)
* `chmod +x /usr/bin/tupload`
* `vim /usr/bin/tupload` (or mcedit, or nano, or emacs, or anything you want, really)
 * Edit the default server and port.
 * If your OS isn't in the list, add your OS and the clipboard method.
 * If you want the default to be `--string`, change the `UTIL` from `cat` to `echo`
 * If you want the default to be `--noclip`, change the `NOCLIP` to `true`
* Ready to go!

### License

Licensed under GPLv2. Read `LICENSE` for more information.