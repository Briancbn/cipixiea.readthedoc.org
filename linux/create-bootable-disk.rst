.. _create_bootable_usb_disk:

Create Bootable USB Disk
========================

.. _rufus_windows_macos_linux:

Rufus (Windows, MacOS & Linux)
------------------------------

`Ubuntu official documentation`_ provide a wonderful guide on creating bootable
USB on Windows with `Rufus`_.
Follow it step by step, you will have yourself a ready Ubuntu bootable USB Disk
in no time!!!

.. _Ubuntu official documentation: https://tutorials.ubuntu.com/tutorial/tutorial-create-a-usb-stick-on-windows#0
.. _Rufus: https://rufus.ie/

.. _startup_disk_creator:

Startup Disk Creator (Ubuntu)
-----------------------------

Open a terminal ``Ctrl+Alt+T`` and type in the following command to make sure
**Startup Disk Creator** is already installed.

.. code-block:: bash

   sudo apt install usb-creator-gtk

Then you can launch the application from terminal just typing
``usb-creator-gtk``.
You can also search for **Startup Disk Creator** in the
**Ubuntu Activity Center**.
After launching the application, you will see the following window.

.. image:: usb-creator-gtk.png

Note that files ending with ``.img`` and ``.iso`` files will be automatically
detected once they are inside the ``Downloads`` folder.
Now plugin you USB drive and press on ``Make Startup Disk``.
Then just sit and wait till the whole process to complete.
