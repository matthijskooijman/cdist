cdist-type__init_script(7)
==========================
Use the init scripts

Daniel Roth <dani-cdist--@--d-roth.li>


DESCRIPTION
-----------
This type can be used to control your init scripts.


REQUIRED PARAMETERS
-------------------
mode
   Specifies what shall be done with the init script (usually one of 'start'|'stop'|'restart'|'reload' or 'force-reload')


OPTIONAL PARAMETERS
-------------------
script
   If supplied, use this as the init-script.
   Otherwise the object_id is used.

base_dir
   If supplied, this type uses this directory instead of '/etc/init.d'. The parameter will not need an ending slash.


EXAMPLES
--------

.. code-block:: sh

    # Reloads the configuration for lighttpd 
    __init_script lighttpd --mode force-reload

    # Reloads the configuration for lighttpd 
    __init_script lighty --script lighttpd --mode force-reload


SEE ALSO
--------
- `cdist-type(7) <cdist-type.html>`_


COPYING
-------
Copyright \(C) 2011 Daniel Roth. Free use of this software is
granted under the terms of the GNU General Public License version 3 (GPLv3).
