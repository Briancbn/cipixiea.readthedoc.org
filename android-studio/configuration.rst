Configuration
=============

Setup Debug USB
---------------

Just follow the `offical guide <https://developer.android.com/training/basics/firstapp/running-app#RealDevice>`_.
You can setup Debug USB in no time.
Also, don't forget to setup `user permission and udev rules <https://developer.android.com/studio/run/device#setting-up>`_.


Setup AVD (``/dev/kvm not found``)
----------------------------------

Most PCs should not have problem setting up AVD.
However, sometimes CPU virtualization is not turned on by default.
If you find this error ``/dev/kvm not found``, here is what you need to do.

#. **Check CPU's Support for Virtualization**

   Install **cpu-checker**,

   .. code-block:: bash

      sudo apt install cpu-checker

   Then run the following command to check whether you CPU support
   virtualization.

   .. code-block:: bash

      sudo kvm-ok

   You will see whether virtualization is supported from the console output.

#. **Enable Virtualization in BIOS**

   This varies between CPUs and Motherboards.
   Google is probably the best place for answers.
   You will need to **reboot** your computer and log into **BIOS** to change
   the configuration of the motherboard.
   In my case, I was using a AMD CPU with ASUS motherboard.
   What I did was enable the **SVM** options under the **Advanced Tab** inside
   my BIOS.
   (`Reference <https://www.asus.com/support/FAQ/1038245/>`_)

#. **Install KVM**

   Install KVM through APT running the following command.

   .. code-block:: bash

      sudo apt install qemu-kvm

  After the installation is completed, you need to enable non-root access to
  ``/dev/kvm``.
  Thus you can add your username to the ``kvm`` group with the following
  command.

  .. code-block:: bash

     sudo adduser "$USER" kvm

  Now after finishing all the commands above, you can run ``kvm-ok`` once
  again. This can run it under the **non-root** setting.
  You should be able to see the following output.

  .. code-block:: bash

     $ kvm-ok

     INFO: /dev/kvm exists
     KVM acceleration can be used

Now you can go back to you Android Studio AVD manager to finish the setup of
the simulation.
