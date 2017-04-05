Objects
=======

Objects are entities in the game that correspond to Rock Raiders, monsters, vehicles, resources, and buildings.

Each object is defined in the game engine and configured via Lego.cfg, and placed in
levels via their corresponding ``.OL`` (Object List) files.

Objects are referred to in configuration using internal names, a table of which is given below.

Many properties are configurable, such as the number of upgradable levels, the parameters of each level (e.g. the time it takes to drill through various kinds of rock, the speed of the object over various kinds of terrain, etc.), whether or not they can move on lava or water, and so on.

Internal Object Names
~~~~~~~~~~~~~~~~~~~~~

The game engine uses its own names (specified in Lego.cfg and the engine itself) for objects.
Here is a table of internal names to real names, from Lego.cfg (see the ``ObjectNames`` section.)

==============    ==============================
   Internal         In Game
==============    ==============================
LargeMLP            Large Mobile Laser Cutter
Hoverboard          Hover Scout
SmallHeli           Tunnel Scout
SmallMLP            Small Mobile Laser Cutter
SmallCat            Rapid Rider
SmallDigger         Small Digger
SmallTruck          Small Transport Truck
BullDozer           Loader Dozer
WalkerDigger        Granite Grinder
LargeDigger         Chrome Crusher
LargeCat            Cargo Carrier
LargeHeli           Tunnel Transport
Pilot               Rock Raider
RockMonster         Rock Monster
TinyRM              Small Rock Monster
TinyIM              Small Ice Monster
SmallSpider         Small Spider
bat                 Bat
Slug                Slimy Slug
Lavamonster         Lava Monster
Icemonster          Ice Monster
Barracks            Support Station
GEO-Dome            Geological Center
Powerstation        Power Station
OreRefinery         Ore Refinery
TeleportPad         Teleport Pad
Docks               Docks
TeleportBIG         Super Teleport
Toolstation         Tool Store
Gunstation          Mining Laser
Upgrade             Upgrade Station
PowerCrystal        Energy Crystal
Ore                 Ore
ProcessedOre        Building Stud
ElectricFence       Electric Fence
Path                Power Path
==============    ==============================
