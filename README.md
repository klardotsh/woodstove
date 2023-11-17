# woodstove: declarative unix, without the phd requirement

This document is a sketch, a draft, a brain-dump, an initialization of a project
I hope to some day have the time and energy to finish.

---

All of this of course implemented in [gale](//sr.ht/~klardotsh/gale) :)

^ includes package definitions, perhaps use an ffi-codegen hack within the
compiler to "compile to" apks?

Use APK file format from Alpine, or at least some fork thereof. For that
matter, use `apk-tools` or a white-room non-GPL implementation thereof, because
it's a beast of a package manager.

USE flags are a great idea from Portage (and somewhat XBPS), use them! You know
what else Portage did right? Atoms: `dev-lang/python-3.12-r1`.

System always tries to have exactly one copy of everything installed.
`python3.12 +sqlite +tk` fulfills `python3 +sqlite`. This implies our solver
has to be extremely permissive, and of course must also solve on multiple axes:
not just versions, but also USE flags. Portage is probably a great source of
inspiration here, but their code is GPL, and so we'll have to come up with
everything on our own.

Desktops are primary target. If you make it easy on a desktop/laptop, servers
should fall right in line.

Encrypted rootfs should be a first-class citizen.

Automatic creation and updates (only when safe) of filesystems given a partition
layout???
