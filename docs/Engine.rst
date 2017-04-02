Engine
======

The Lego(R) Rock Raiders game engine was fairly unusual for the time, using DirectX 6 in `retained mode <https://en.wikipedia.org/wiki/Direct3D#Direct3D_2.0_and_3.0>`_.
It was one of a very limited amount of commercial games to do so (it later became deprecated and eventually dropped from Windows Vista,
which makes it inconvenient to play on modern machines -- ``d3drm.dll`` is required.)

Besides Direct3D 6, it also uses DirectDraw (presumably for the UI and video rendering), and DirectInput for input handling.

It is rendered with a 16-bit color depth in 640x480 resolution, and the interface is partially configurable:
resolution-dependent interface images are defined in ``Lego.cfg``, by default only supporting 640x480.

However, some interface elements such as the oxygen meter are in a hardcoded position and cannot be changed without modifying the
game executable.

The rendering engine does not support `transluscency <Textures.rst>`_ very well, resulting in the background or other objects being rendered in
the alpha part of textures instead of what's behind it.
(They likely do not sort the render queue to separate transluscent/opaque objects, or disable depth testing when drawing transluscent objects.)

Random Facts
~~~~~~~~~~~~

- The version control system used was Visual SourceSafe
- The developers used a Windows share named ``MOTHER`` (located at ``\\MOTHER``)
- The game loads assets up front, which is why it's so slow to load at startup
