# 3 - Controls

Now that you have your mouse settings it's time get the keyboard settings.
But first, a bit about _.cfg_ files (for those who aren't familiar with them). Inside _.cfg_ files you can have all your game settings (mouse, keyboard, graphics, internet,...), scripts (kinda like macros except it's in the game) and more.

The _config.cfg_ is created at first launch. It's the first file to be read by TF2 (_autoexec.cfg_ comes right after it) and it holds all settings for TF2. Although you can change it to have your settings, it is not recommended as it will be overwritten when TF2 launches again (unless you set it to read-only mode, but even on read-only mode it will be overwritten when updates come in).

The best way is to have your settings in your _autoexec_ (or several files). If you use other files besides _autoexec_, you call them (tell TF2 to execute them) like this:
```source-scripting
exec <filename>
```
So, for example, if you have your binds in a different file called _binds.cfg_ you call it from _autoexec_ like this:
```source-scripting
exec binds // without the .cfg (file extension)
```
_**NOTE:** the two slashes ("//") indicate the beggining of a single line comment, everything afterwards on that line isn't read by the game, you can write w.e. you'd like here_

## 3.1 - Binds

This is pretty easy. Open TF2, choose the key bindings in-game and save. Done.
If, however, you want something more complex, open your _config.cfg_ (after you've done the steps above), in your _cfg_ folder, copy all the lines starting with a "bind" (and the "unbind all" command - _"unbind all" unbinds all keys so make sure to have it before all the bind commands_) to your _autoexec.cfg_ (or another file like explained above). Now that you have a copy of all the bindings you can play with them.

The way to use the _bind_ command is simple:
```source-scripting
bind [key] [command] // binding one command to a key
bind [key] "[command1]; [command2]" // binding two or more commands to a key
```
More about the _bind_ command [here](https://wiki.teamfortress.com/wiki/Scripts#Bind "Binds - TF2W").

An example of how to use binds: I don't use the mouse wheel to change between all weapons, instead, I use it to change between primary and melee only. This code does that:
```source-scripting
bind "mwheelup" "slot3" // this binds wheel up for melee
bind "mwheeldown" "slot1" // this binds wheel down for primary
```
Here is a [list of key names](https://wiki.teamfortress.com/wiki/Scripts#List_of_key_names "List of Key names - TF2W").
