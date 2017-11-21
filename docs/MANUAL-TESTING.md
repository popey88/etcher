Manual Testing
==============

This document describes a high-level script of manual tests to check for. We
should aim to replace items on this list with automated Spectron test cases.

Image Selection
---------------

- [ ] Cancel image selection dialog
- [ ] Select an unbootable image (without a partition table)
- [ ] Attempt to select an unsupported image
- [ ] Change image selection

Drive Selection
---------------

- [ ] Open the drive selection modal

Image Support
-------------

- [ ] Flash an uncompressed image
- [ ] Flash a Bzip2 image
- [ ] Flash a XZ image
- [ ] Flash a ZIP image

Flashing Process
----------------

- [ ] Close the application while flashing using the window manager close icon
- [ ] Close the application while flashing using the OS keyboard shortcut
- [ ] If applicable, close the application from the terminal using Ctrl-C while
  ashing
- [ ] Force kill the application (using a process monitor tool, etc)
- [ ] Cancel the application close warning dialog

In all these cases, the child writer process should not remain alive.

- [ ] Kill the child writer process, and check that the GUI reacts
  appropriately
- [ ] Flash consecutive images without closing the application
- [ ] Disable validation and flash an image
- [ ] Go to the settings page while flashing and come back

Global
------

- [ ] Close application from the terminal using Ctrl-C

Elevation Prompt
----------------

- [ ] Flash an image as `root`/administrator
- [ ] Reject elevation prompt
- [ ] Put incorrect elevation prompt password
- [ ] Enable unsafe mode, and check drive selector dialog

Unmounting
----------

- [ ] Disable unmounting and flash an image
- [ ] Flash an image with a file system that is readable by the host OS, and
  check that is unmounted correctly

Known Problematic Regressions
-----------------------------

- [ ] Click "Flash", cancel elevation dialog, and click "Flash" again
