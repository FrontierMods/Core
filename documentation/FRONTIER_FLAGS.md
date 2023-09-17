# Frontier Mods flags

Flags are sorted alphabetically.

Use `Ctrl+F` to find specific flags faster.


## `CARD_STANDARD`

**In-game description**: "This item has the right dimensions to be stored in <info>credit and ID card compartments</info>."

There exists an international standard for ID cards: ISO/IEC 7810 ID-1. It dictates the exact dimensions and deformation tolerances, but not uses or weight, of most cards operating today. This includes company ID cards, driver's licenses, credit cards, and many more.

The intended use for `CARD_STANDARD` is to signal the card's adherence to the standard, thus allowing it to be accepted by small dedicated pockets, such as those in wallets, organizers, and dedicated pockets in wearable storage.


## `MOLLE_DECOR`

**In-game description**: "This item is a decorative piece for the <info>MOLLE gear system</info>. It can be attached to <info>MOLLE carrying equipment</info>, such as a vest or a backpack.  It does not provide any benefit beyond asserting you into the empty world."

(See [`MOLLE_POUCH`](#molle_pouch) for the description of the MOLLE system itself.)

MOLLE decorative panels use the `MOLLE_DECOR` flag, allowing them to be attached to a dedicated velcro panel on some MOLLE equipment. MOLLE webbing itself does not accept these. Not all MOLLE-enabled items also have decorative panels.

In real-life combat, these panels can be used to identify soldiers and their important vitals, such as blood type.

In a post-apocalyptic situation, these panels offer no pragmatic benefit. Their primary role in *Cataclysm* is self-expression: you can attach to your equipment whatever panels that suit your personality.


## `PAPER_FILE_SIZED`

**In-game description**: "This item has the right dimensions to be stored in <info>file compartments</info>."

Paper-file-sized items are usually maps and paper sheets. These may also occasionally include comic books, thin journals, newspapers, and leaflets.

These are the items that comfortably fit in dedicated and improvised file storage and can be easily extracted from it. The latter is controlled by the specific pocket's settings, via the `item_min_length` property, which may prevent documents that are too short from entering the pocket, because extracting it afterwards may prove difficult.

The intended use for `PAPER_FILE_SIZED` is for admin pouches, organizers, and other file containers.


## `SHOULDER_RIG`

**In-game description**: "This item is worn on your shoulders. It can hold up to two <info>shoulder rig modules</info>, such as pistol holsters or magazine pouches, on your torso."

Shoulder rigs are wearable structures of leather or cotton, worn around the shoulders, usually to hold a firearm and/or magazines for one in a concealed fashion. Shoulder rigs are typically employed by law enforcement officers, whose job requires maintaining a formal or civilian appearance without overt displays of combat readiness.

Shoulder rigs come in two varieties: pre-assembled and modular.

The primary use of the `SHOULDER_RIG` flag is for the latter: it indicates to the player that the rig is modular. The `SHOULDER_RIG` alone is not enough to enable rig modularity. The `SHOULDER_RIG_MODULE` flag (see [`SHOULDER_RIG_MODULE`](#shoulder_rig_module)) is used to filter allowed items inside the rig's pockets.

Pre-assembled / non-modular shoulder rigs **should not** use this flag.


## `SHOULDER_RIG_MODULE`

**In-game description**: "This item is a <info>shoulder rig module</info>. It can be attached to a shoulder rig and used as a piece of carrying equipment."

Modular shoulder rigs (see [`SHOULDER_RIG`](#shoulder_rig)) rely on using special pockets to be effective. These are referred to as shoulder rig modules.

These modules may host a number of items, most often small fireams (such as pistols and revolvers, and – rarely – compact submachine guns) and related magazines. Modules to carry other sorts of items exist but are uncommon, and never used in the fields of work where a shoulder rig is required.