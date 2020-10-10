Installation
============

Here I will only cover the installation on a Linux machine, since this is my
daily driver.
I will go over the some of the problems that I face installing Android Studio
on Ubuntu and their solutions.

First, install **Java JDK**.
If you are on **Ubuntu 20.04**, you should install **jdk-11**.

.. code-block:: bash

   sudo apt install openjdk-11-jdk

This will install the corresponding JRE (Runtime environment) as well.
You can run the following command to check the Java version

.. code-block:: bash

   java --version

.. note::

   Since the alternative is using **snap**, I actually recommend using **APT**.

#. **Using APT(Advanced Package Tool)**

   After installing the Java JDK, you can run the following commands to install
   Android Studio.

   First setup additional source list.
   Although this PPA might look suspicious, this is actually the official
   Android Studio binary release PPA for Ubuntu.

   .. code-block:: bash

      sudo add-apt-repository ppa:maarten-fonville/android-studio
      sudo apt update

   18.04 onward, ``sudo apt update`` is actually not needed any more, since
   it is run automatically after ``add-apt-repository``.

   Now, install android studio through APT.

   .. code-block:: bash

      sudo apt install android-studio

   Now you launch the application through **Activities**.
   Follow the setup guide to finish the installation.


