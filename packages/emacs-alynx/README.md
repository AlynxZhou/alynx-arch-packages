emacs-alynx
===========

This is just used to record my building options, it may be not OK for you. I even do not upload it to AUR. If you try my package and crash, don't cry to me or upstream devs.

Based on <https://aur.archlinux.org/packages/emacs-pgtk-native-comp-git> and <https://gitlab.archlinux.org/archlinux/packaging/packages/emacs/>.

To remind me what I have done:

- Unstable branch, because of some bleeding edge features.
- Use PGTK by default. (No more GUI toolkit hacks and Wayland support!)
- Native compilation, and AOT compile all Emacs lisp files. (Why not?)
- ALSA support. (Why not?)
- XInput2. (But it seems that PGTK does not use it.)
- No CLI or NOX build, I'm a desktop engineer and always have GUI.
- I don't use xwidgets, but may be useful in future.
- No PDF or HTML docs, I just read them directly in Emacs.
- Disable PGTK X warning, I hack GTK and I know what I am doing.
