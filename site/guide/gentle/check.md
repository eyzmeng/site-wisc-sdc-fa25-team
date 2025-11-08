# Self-check your ’puter knowledge!

Some basic stuff that is nice to know in general...

## Part 0: Know your system

Depending on your operating system, the commands you run may be different.
macOS (since OS X, which has been the case for quite some decades) and
Linux are Unix-likes, but Windows NT is a descendent of MS-DOS.  So in
terms of userspace interface, macOS and Linux are most similar.

For the purpose of simplification, I will assume that this team uses either
Windows, macOS, or any major Linux distribution, and that they are somewhat
recent.  If you are using an operating system not listed here, do let me
know so I can look into it (and I apologize for my ignorance in advance).

For Windows in particular, Windows 10 or newer would be nice since it ships
with a built-in OpenSSH client.

### The Terminal / Console / Command-Line / Shell

*In this section, "Unix" means it applies to both modern macOS and Linux.
Unless explicitly noted, the text applies to Unix.*

* The terminal is a device that lets you interact with programs by
  typing stuff into it.  It is one of the oldest computer interfaces,
  but also the most universal of them all.  Physical terminal devices
  (TTY) are rare these days, but typing is nice (you may debate that
  but, for the sake of my narrative, *don't*) so, in order to keep
  the same interface, people invented *pseudo*-terminals (PTY), where
  you get to do all the nice typing even without the mechanical stuff.
  A program that does this is called a *terminal emulator*.

  In Windows, something similar happens except I don't get to use all
  these fancy terms; all I know is they do it somewhat differently.
  (Namely, they are still called terminal emulators, but Windows has
  no concept of TTY and PTY (not before [ConPTY][] at least).

  [ConPTY]: https://devblogs.microsoft.com/commandline/windows-command-line-introducing-the-windows-pseudo-console-conpty/

* In Unix, terminal (TTY) drivers by default operate in [cooked
  mode][].  The analogy of our interest here is that when you type
  certain key combos, the drivers intercept them instead of just
  passing them as raw control characters --- "un-cooked" in other
  words.  (I wonder who comes up with these terms... anyways.)

  Perhaps the most important control sequence you should know is
  Control-C (which I will denote as **^C** for brevity: that is,
  ^ stands for the control key):  ^C instructs your computer to
  send a [keyboard interrupt][] signal to the program that is
  running (also known in libc as [SIGINT][]).  Unless the
  program chooses to handle the signal, the kernel immediately
  terminates the program.
  
  Some control characters are sent literally.  For instance,
  ^M sends carriage return (U+000D, `"\r"`), which returns the
  cursor to the beginning (hence the name carriage *return*).
  Combine this with the line feed (^J, U+000A, `"\n"`) which
  moves a virtual roll of paper upward (like a typewriter),
  and you get the standard end-of-line sequence: CRLF, or `"\r\n"`.

  Of course, it would be unfortunate if pressing the Enter key
  (which sends ^M) only moved the cursor back without moving it
  down to the beginning.  That's why the drivers in cooked mode
  actually translates ^M into ^M^J *behind the scenes*, so you
  can still press just enter and it works just as you would
  expect.  (For the interested readers, consult the manual page
  of [**stty**(1)]() in your system. ;)

  [cooked mode]: https://stackoverflow.com/a/13104585/19411800
  [keyboard interrupt]: https://en.wikipedia.org/wiki/Keyboard_interrupt
  [SIGINT]: https://man.openbsd.org/signal.3#SIGINT
  [**stty**(1)]: https://linux.die.net/man/1/stty

[Common](Common) in both Unix and Windows is something called a *prompt*.
You very likely have heard of this: it's the string of text
just before the cursor that *prompts* the user to type something.
The difference is that prompts in terminals don't usually look
like this:

```
Type something..... NOW!!! >>>> _
```

or this:

```
I am patiently waiting for you to enter a command.  Please type
them below and feed your terminal a carriage return (^M or Enter),
so that I can receive it on my end and process it.  _
```

but usually something like this:

```
PS C:\Users\blablah> _          # This is PowerShell's prompt!
C:\WINDOWS\system32> _      & REM This is CMD.EXE's prompt
```

or

```
[user@a-puter ~]$ _
[root@a-puter /]# _
```

even worse than that:

```
$ _
# _
```

(Yes, that `$` or `#` *is* a prompt!  Do not be fooled by its reticence!!!)

Also common in both Unix and Windows is the concept of a *current
directory*.  This is commonly displayed as a part of the *prompt*,
but you can explicitly tell the command to show it.


### Package Manager

### Flavors of Text Files


## Part 1:
