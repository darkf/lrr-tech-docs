Models
======

The game uses LightWave 3D v5.0 and v5.6 for models and animation. [1]_

For models, the file format is ``.LWO`` (LightWave Object) which should
start with the the magic identifier ``FORM``, since it is a
``FORM``-based `Interchange File Format (IFF) <https://en.wikipedia.org/wiki/Interchange_File_Format>`_ format file.

The version of LWO used is called ``LWOB`` (version 1). Later versions
of LightWave use a newer format, so it is crucial to use the right
version (newer editions of LightWave 3D can export to the older formats,
with some caveats.)

Documentation for LWOB is provided at [2]_.

Note that v5.0 did not support UV maps, and as a result UV maps are
stored separately [1]_  (presumably in ``.uv`` files, but this is
unverified.)

Scene / Animations
------------------

Scene files are compositions of models together with metadata and
animation keyframes. They are given the format ``.LWS`` (LightWave
Scene), and the version is v1. The magic identifier should be ``LWSC``.

Documentation for LWSC is provided at [3]_.

Which scene files are used for which objects (and for which animations)
is defined in the object's ``.ae`` definition file.

Footnotes / References
----------------------

.. [1] Developer's comments –- http://www.rockraidersunited.com/topic/2132-wow-people-i-am-both-stunned-and-impressed/?do=findComment&comment=44624

.. [2] www.martinreddy.net/gfx/3d/LWOB.txt

.. [3] www.martinreddy.net/gfx/3d/LWSC.txt
