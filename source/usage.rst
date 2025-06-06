Using the FlippyDrive
*********************

.. _sdcard:

SD Card
````````````````

You can use any SDHC/SDXC card with FlippyDrive. We do not suggest using SD Cards with a capacity less than 4GB as those may have compatibility issues.

.. _sdcardsetup:

SD Card Setup
------------------

In order to use the FlippyDrive you must first format the SD card or configure Wi-Fi to target a desktop machine.

.. todo
    Wi-Fi configuration is in internal testing and will be available shortly

Make sure your SD card is formatted with exFAT or FAT32. We suggest using exFAT as it is a more modern standard.

.. _sdcardfiles:

SD Card Files
------------------

Once your SD card is formatted you can place supported files in the root of the SD card.

Supported files are:
    - ``.iso``
    - ``.fdi``
    - ``.gcm``
    - ``.dol``
    - ``.dol+cli``

.. note::    
    If you have a ``.nkit`` file, just rename it to ``.iso``.

    ``.rvz`` will be supported in the future but **only** through Wi-Fi or Ethernet due to hardware limitations.

.. _usage:

Usage
````````````````

Now that you have your SD card setup you can insert it into the FlippyDrive and power on your GameCube.

.. _startup:

Startup
------------------

When booting the GameCube using FlippyDrive you have three options:


.. _updatemode:

Bootloader menu
---------------

If you hold down the :kbd:`X` button on the P1 controller it will start the FlippyDrive :doc:`bootloader`.

.. _discmode:

Disc Mode
=========
.. versionchanged:: 1.5.0
   In version 1.4.3 and below, the :kbd:`L` and :kbd:`R` triggers were used for Disc Mode and Enhanced Disc mode (also called passthrough/bypass - as it lets all of the disc drive information pass through the FlippyDrive). It was moved to the +Control Pad to avoid controller calibration issues while powering on the system.

Two disc modes are provided by the FlippyDrive to launch games in the physical disc drive.

Hold ``Left (←)`` on the +Control Pad (Player 1) when powering up the console to enter Disc Mode.

Control is handed completely to the physical disc drive and the disc will load as if no FlippyDrive is installed.  That means your disc and console must match regions and no additional features are available as this is stock GameCube behavior.

Once control is handed off to the drive in Disc Mode, it is not possible to exit unless you power off the GameCube.

Enhanced Disc Mode
==================

Hold ``Right (→)`` on the +Control Pad (Player 1) when powering up the console to enter Enhanced Disc Mode.

This process uses your physical disc loaded via cubeboot with the ``config.ini`` file with read with appropriate video and region-free settings applied.

.. _cubeboot:

Normal Mode
-----------

If you do not hold down any buttons while the GameCube is turning on, it will boot directly into Cubeboot. However if you have placed a ``boot.dol`` file in the root of your SD card it will boot that program instead.

Cubeboot will play the GameCube startup animation and then jump directly into the Cubeboot Loader which allows you to select a game to play.

You can navigate the loader with the analog stick and press :kbd:`A` to select a game. If you do not want to start that game simply press :kbd:`B` to get back to the list of games.

Once you are ready to play, press :kbd:`START` on the game select screen and it will immediately boot the game.

Multi-disc games
----------------
When a game requests another game disc to be loaded, as long as the disc image is available from the current source (SD or network) it will load the disc within a few seconds.

.. seealso::
  - If you experience any issues during gameplay please reference the :doc:`compatibility` page and submit a bug report using the form.
  - For FlippyDrive bugs go to :doc:`troubleshooting`.
  - For Game related issues while using FlippyDrive check :doc:`compatibility` and submit a bug report.
  - For more information on configuring the FlippyDrive check the :doc:`configuration` page.

.. toctree::
    :hidden:

    updates
    bootloader
    backup
    memcardprogc
