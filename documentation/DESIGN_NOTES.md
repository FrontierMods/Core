# Design Notes

## Realism Score

### What realism score represents

Modding, by its very nature, expands the breadth of fiction genres a game could accomodate. In our case, the base game could reasonably be made into anything from high fantasy to gritty realism to space opera. Each mod can operate on their own level of desired realism. This is evident in the mods that come with the base game, as well as third-party mods. For some players, it might be important to pick mods that don't clash when played together; for example, only mods that add fantasy and magical elements, or mods that add anything but magic.

Thus, Frontier Mods uses realism score scale in order to inform the player about the experience they will get, genre-wise. The scaling is between 1 and 5, inclusive. Realism score can be given as a single value or as a range, depending on the nature of the mod. Note that submods may have realism scores that are different from their parent mods.

- 1 is for things that are completely fantastical in their nature, where no social, cultural, or scientific concept could explain their inner workings or even existence
- 2 is for concepts where an attempt has been made to ground them in reality, but the result is still largely in the realm of fiction; sci-fi or fantasy ideas with but one foot in reality as we know it
  - Foundation
- 3 is for content where noticable liberties have been taken to render the desired objects, while maintaining as much groundedness in reality as possible; sci-fi or fantasy ideas bordering on realism
- 4 is for items that are mostly grounded in reality, with freedoms taken to their in-game rendering due to conceptual limitations (e.g. inability to get accurate measurements of real items in the category, or limited public knowledge on how a thing operates)
  - Dapper
  - Computation
- 5 is for stuff that gets modelled as realistically as possible, with respect to its functionality, physical dimensions, name, description, and other aspects, as far as the game engine would allow
  - Loadout
  - Armory

## Auditing

### Why audit?

One of the most common questions received about Frontier Mods is: why not integrate these changes to the base game?

There are several answers.

#### Stable-version design

These mods are developed for stable versions of the game only. This means it might take more than a year for audits to go through and be usable by Frontier Mods. In the meantime, there would have to be an accessible repository of audits for the mods to rely on.

In other words, audits of item dimensions might as well remain in the Core mod, where they will be accessible to the rest of the mods indefinitely.

#### Arbitrary nature of audits

While the overarching goal of Frontier Mods is to bring groundedness and realism to the design and implementation of items, and while audits' primary purpose is to support this goal, the target real-life items chosen for modelling off of are arbitrary. Carefully-chosen based on the best available knowledge, but still arbitrary.

This means that the core development team of _DDA_ may not agree with the choice of base items, which would likely preclude inclusion of some, if not all, audits.

#### Effort and anxiety

Adding pull requests with suggested audits is, while not difficult, also not momentary. It requires forking the game repo, making the necessary changes, then writing a relatively-length report on what's been done, why, and (sometimes) why the chosen approach is the best for a particular problem.

In addition to that, there's a notion of anxiety associated with adding any degree of change to a large project, the design direction of which is squarely guarded by a core team of developers, who in all cases get a final say on what find its way into the game.

All of this means there's a significant amount of effort associated with adding or changing content with the base game – effort that, in an already-dwindling personal-energy economy, has proven to be too much to be worth it. The developers of Frontier Mods would rather focus on the mods themselves, in an environment where confrontation is not anticipated and where freedom of creativity is plentiful.

#### Can I port these audits to the base game?

Absolutely. The licensing of all Frontier Mods had been chosen in order to enable others the same degree of creativity as the mods themselves utilize. You don't need to seek permission in order to port any part of the mods to the base game; according to the current license (MIT), you can freely modify and share the mods. (Consult the license itself should you find yourself wondering what exactly is permitted or required.)

### Firearm lengths

By default, _DDA_ uses ferret length (length between two farthest points of an object) for its `longest_side` dimension of firearms. While it's undoubtably a valuable number to have, it doesn't work well when the goal is to model holsters – and their capacity – realistically, such as with Armory.

Many of the modern holsters are designed for specific models of pistols. Those that aren't, often have restrictions on what length of pistol they accept. This is usually due to the design of the holster, with retention mechanisms that rely on latching over the back of the pistol's slide. A more-accepting holster's being loose enough to accomodate a variety of pistols also means there's space for the pistol to wiggle about; without a retention strap keeping it in place, it could move to an uncomfortable position (making the draw clumsy) or, worse, find a way out of the holster during a stressful situation.

Frontier Mods choose to obey barrel length restrictions stated by the holsters' manufacturers. For that, the mods must be able to access or infer barrel length and/or overall length of the pistol. Since pockets cannot accept secondary restrictions (such as comparing a custom value of an item), we find remodelling item length for pistols a better – though hardly perfect – solution.
