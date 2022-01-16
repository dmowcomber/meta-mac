# Meta Mac

Enables a Mac OS-like shortcut key experience on Linux.

For an overview of the various key remapping solutions, and Mac-to-Linux switcher options, see my article [Key Remapping in Linux - 2021 Edition](https://medium.com/@canadaduane/key-remapping-in-linux-2021-edition-47320999d2aa)

Works in X & Wayland, and has awareness of which app is focused so that app-specific key combinations can be sent.

# Dependencies

- libudev
- [keyd](https://github.com/rvaiya/keyd) 2.2+

## Installation


1. Install [keyd](https://github.com/rvaiya/keyd)

```
sudo apt install libudev-dev
git clone https://github.com/rvaiya/keyd.git
cd keyd && make && sudo make install
sudo systemctl enable --now keyd
```

2. Run install script

```
./install.sh
```

Done!

## Which Shortcut Keys?

- For cut/copy/paste key combos, translate to universal clipboard keys (works in terminal as well as other apps):
  - Cut: `Command-X` -> `Ctrl-Del` 
  - Copy: `Command-C` -> `Ctrl-Ins`
  - Paste: `Command-V` -> `Shift-Ins`

- Window switching:
  - Switch: `Command-Tab` -> `Meta-Tab`
  - Switch backwards: (when in App Switch mode): ``Command-` `` => `Shift-Meta-Tab`
  - Switch between windows of same app: ``Command-` ``
  - Open the Launcher: `Command-Space`

- Switch directly to an open tab, e.g. Firefox or VS Code:
  - `Command-1` -> `Alt-1`
  - `Command-2` -> `Alt-2`
  - ... etc.

- The remaning `Command-*` key combos are translated to `Ctrl-*`, e.g.
  - Close Window: `Command-W` -> `Ctrl-W`
  - New Tab: `Command-T` -> `Ctrl-T`
  - Bold: `Command-B` -> `Ctrl-B`
  - Italics: `Command-I` -> `Ctrl-I`
  - etc.

- Mouse clicks:
  - `Command-Click` -> `Ctrl-Click`


## Why?

The biggest discomfort I have with Linux shortcut keys is the mismatch between the terminal's idea of copy-paste (Ctrl+Shift+C / Ctrl+Shift+V) and everything else in Linux (Ctrl+C / Ctrl+V). And Linux isn't alone--Windows, too, has a weird relationship with copy/paste when it comes to the command shell. Only on the Mac have I experienced the sensible default that Command-C will copy to the clipboard, and Command-V will paste, regardless of which app is running.

But why stop there? If you have experience with Mac OS and have the ability to make customizations in Linux (and boy, do you!) then why not make switching to Linux as comfortable as possible?

On a personal note, I've lived and worked on a Mac for the past 15 years, and while I still admire Apple's technical and design capability, our values have slowly been drifting apart over the years. Apple is no longer the underdog, and it's clear that it doesn't need to design for the values or culture of software developers any more.

## What hardware/Linux distro do you use?

I'm very excited to joining the free culture movement once again via my first [frame.work](https://frame.work) laptop and [Pop!_OS](https://pop.system76.com/). I've written Meta Mac and collaborated on the [keyd](https://github.com/rvaiya/keyd) project in the hope that it will ease the transition for others along this path as well.

## Thanks

Thanks to Raheman Vaiya of [keyd](https://github.com/rvaiya/keyd) for a great library and for a lot of help.