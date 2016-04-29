# mcimport

This mod converts a minecraft world into minetest.

The process is offline. Minecraft should not be running on the world
that is to be converted. The output should be an empty folder, and
no map.sqlite should be present in the empty folder.

The output is a world folder that is playable, permitted that the
required minetest mods are installed. If mods are missing, you will
encounter "Unknown" blocks in the minetest world.

This mcimport fork was created to improve on the existing mcimport
project, with one significant change: This form aims to create
*playable* minetest worlds where stuff works:

- chests can be used to put stuff in
- doors open and close
- simple mesecons circuits may work
- furnaces work

Also, the assumption is that converted maps are for multiplayer
use, and that the most important motivation for using this
converter is to *preserve* previously custom built objects
and buildings, but *not* meant to preserve the gameplay style
and feel of minecraft. As such, there are numerous blocks that
are *not* converted 1:1 from MC to MT. A good example is Lapis
Lazuli. LL ore will be converted to plain stone, and LL blocks
into blue wool, simply because there is no reasonable equivalent
in MT that is an actually useful block and not something created
purely to copy MC. This project also aims to never convert
blocks to "Unknown" nodes and strives to leave a playable are
that is friendly for users performing a one-time conversion.

- some flowers are approximations
- double plants may end up being single node blocks
- wood types are similarly not an exact copy
- until fixed, beds, doors, fences, walls are likely broken
- signs convert, but MT can't rotate them in 30 degree angles

There are a large number of things that are just never going to
be convertable, and so the following will likely never work and
are therefore converted to air blocks. Entities are readily
spawned by several mob mods in minetest, so conversion is likely
not critical to users, and left out.

- crafting table
- hoppers, dispensers, droppers
- entities


License:

Copyright (C) 2016 - Nore, dgm555, sofar and others

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE X CONSORTIUM BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Except as contained in this notice, the name of the authors shall
not be used in advertising or otherwise to promote the sale, use or
other dealings in this Software without prior written authorization
from the authors.

