servCDN
==========

servCDN is a ShareX webserver implemented in JavaScript designed to upload and serve files. It's modular and anyone can create modules for the server. (If you want to create a module for servCDN, **I'm not providing servCDN documentation for APIs**, but if you are fluent in JavaScript, you should be able to figure out what you need to use. Feel free to write documentation if you're feeling like it too. I'll accept any PRs for it.)

(note: I've used some code from [ravi0lii's ShareX server](https://github.com/ravi0lii/node-sharex-server) for the upload and deletion (as well as the vanity module, which is a copy of the upload function but optimised for transfers). They are adequate enough for use in servCDN, but I've made a few changes for compatibility, security, and some other general changes. I also used some code from Stack Overflow for the random file names.)

### SSL support
If anyone wants to PR SSL support, feel free to. I usually use a reverse-proxy on my dedi with Apache to provide HTTPS support for my CDN, so I won't be implementing this myself.

### Why do servCDN module files end in .so?
I don't know, .so sounds better than .js in my head. servCDN itself is not written in Assembly **at all**.

### I made a module. How can I PR it to the servCDN repo?
servCDN is modular and divides modules into folders (the core and coreutils modules are separated, for example). Modules are stored in mod.d and you can write your modules there.

In terms of modules being added to the servCDN repo, **only modules with core functionality will be accepted to master**. Examples of core functionality modules include SSL modules and password protection modules. **I'll create a second repo for other non-core modules if anyone wants it.**

(**NOTE: You will need to provide a secondary configuration file stored inside mod.d if you would like to PR to the master repo OR the module repo (when that's up).**)