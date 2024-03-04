# Donate to Frontier Mods

Frontier Mods are developed by a single person – [myself](https://github.com/Hyperseeker) – as a project of passion. However, recent events have made my life challenging by taking away stable income I used to rely on for a long time. (Nobody's fault, sometimes bad things happen.) As such, I'd like to use what little platform I have here to call for donations.

The mods under the Frontier umbrella (including small mods over at [Frontier Mods Extra](https://github.com/FrontierModsExtra/)) will forever remain free and open-source. They are, after all, a work of passion, to be shared with everybody. However, what I'd like to offer is a way to influence the mods' development in a way that's personalized, fun, and (hopefully) enticing.

## The Benefits of Donating

Each donation contributes to my well-being, by allowing me to pay rent, buy food, and (occasionally) treat myself to a nicer meal. My lifestyle is very small; it doesn't take a lot to afford, but right now, even that is under question.

Beyond that, because I love working on these mods, donating helps me keep doing that in my spare time.

As such, each donation (unless requested otherwise by the supporter) will be honored publicly. For non-specific donations (i.e., to Frontier Mods in general), you will see your name in the README file of this mod (Frontier Core, used by every Frontier mod, though not necessarily Frontiers Extra mods). For specific donations (i.e., to Armory, or Remedy, or Handload), your name will appear in the README file of that mod.

In order to make a specific donation, you should mention the mod you're intending to support alongside your donation. If your chosen method of donation does not include a way to send a message alongside it, you can contact me via any of the methods outlined below, with a proof of donation, in order to specify the mod you're donating to support. If you don't, I shall assume you donated to support Frontier Mods in general.

## The Ladder of Benefits™

Here are the enticing options I mentioned previously:

For each donation above €15 (or the equivalent in the currency of your choice), you can suggest one item variant that you'd like to see in the game. Given the breadth of domains Frontier Mods covers, it could be any of the items I've (re)worked, provided it's:

1. mechanically-possible (the game allows the item to have variants, and the latest stable release of the game features the variant type)
2. within the spirit of the game and the mod that features the item (both of which take a grounded, realistic approach, while occasionally enjoying themselves with a fun little twist here and there)
3. within the limits outlined below

(See a section below for what mods and items you can choose.)

The 15-euro threshold is the first step of the Ladder of Benefits™. You can think of the ladder as a system of tiers for one-time donations, similar to the tiers of support subscription-based donation platforms (like Patreon) use.

- donations of **€30 and higher**: one more variant, for a total of two variants
  - could be two variants of the same item, or one variant each for two items
- donations of **€50 and higher**: a new item that fits the concept of the mod, _or_ one more variant, for a total of three variants
  - the new item will be modelled with the variants it has listed in the official store
  - if there's only one variant listed in the official store, you can suggest two extra variants for it
  - if there's more than one variant listed in the official store, you can suggest one extra variant for it
  - if the item has no official single source of design (e.g. it's an old firearm)
- donations of **€100 and higher**: up to three new items within the same set, _or_ two more variants, for a total of five variants
  - "same set" here means "items that are linked to one another by type, class, era, or function, among other things", with a bias towards more-specific sets over less-specific ones
  - examples include:
    - Finnish rifles of the 20th century
    - gear worn by US soldiers during the Vietnam war
    - popular Sicilian dishes
    - early-2000s cell phone models
- donations of **€200 and higher**:
  - **all of the following**:
    - a complex feature for an existing mod, _or_ a new small mod
    - up to five new items within the same set, _or_ two more variants, for a total of seven variants
  - examples of complex features for an existing mod (based on existing or planned features)
    - expanded bandage and gauze system (Remedy)
    - QASM modular equipment interface and de-/reconstructable chest rigs (Armory)
    - custom handloading with stats derived from bullet, powder, and casings used (Handload)
  - examples of small mods:
    - [Hellfire](https://github.com/FrontierModsExtra/Hellfire)
    - [Playing Cards](https://github.com/FrontierModsExtra/PlayingCards)

Note that all progress on supporter-suggested variants, items, and mods will be tracked publicly, in a project of the Frontier Mods account and/or whatever other tools are appropriate for such a duty.

## How to Donate

You can use the following pages to make a one-time donation:

- [Ko-Fi](https://ko-fi.com/frontiermods)
- [Buy Me a Coffee](https://www.buymeacoffee.com/frontiermods)

You can also donate via cryptocurrency:

- BTC: `bc1qxcjh2fx3sm9warety6pjh5yhqrkf36rq8a8zvu`
- ETH: `0x761e626AB32E109cA00Aa209EC92026111B618a6`

## The Outline

The following section goes into detail about the definitions, possibilities, rules, limitations, and a certain degree of guidance when it comes to implementing new things.

### What is a "variant"

A _variant_ of an item is one of the ways it may appear to the player in the game.

With the game's ongoing development, what a variant is specifically is a fluid topic. As of the time of my writing this, there are three types of variants:

- `generic`: variants of this item will appear randomly every time the item is generated. My favorite example of this is the [coffee mug](https://cdda-guide.nornagon.net/item/ceramic_mug). With `generic` variants, the player can only find the variants, not the base item itself.
- `gun`: variants of this item will only appear if the corresponding option ("Show gun brand names") is on (or `True`). While items with this variant type are _generally_ firearms, they can be used to enable similar behavior for other items. Armory, the mod about tactical gear, uses `gun` variants on worn items (such as chest rigs and MOLLE pouches) in order to turn "generic" (if realistically-modelled) items added by the mod into their brand-name counterparts.
- `drug`: same as with `gun`, but for medication: turning [generic drugs](https://en.wikipedia.org/wiki/Generic_drug) into their brand-name counterparts if the corresponding option ("Show drug brand names") is enabled in the settings. (Note that this variant type does not exist on the latest stable release of the game – in this case, 0.H, which the mods aim to support – so you may not specify it as the variant type of your suggestion.)

This is what the Ladder of Benefits™ refers to when giving you the option to add a new variant. Variants of the same item share the same properties, including weight, size, length, pocket capacity etc.. Note that this means that an item which is larger, smaller, lighter, heavier, or otherwise physically- or mechanically-distinct (e.g. it looks exactly like a different item, but does something the original item doesn't) is, technically-speaking, a different item and not a variant.

### What variants go

Both the base game (in its latest iteration) and Frontier Mods generally aim to present a realistic, grounded world, where its contents make sense to someone who lives in the real world.

However, I recognize that modelling different types of historical camouflage may not appeal to everybody the same way, and that some variety and some fun must be had in order to keep the game enjoyable. As such, variants that may be considered cute, silly, outlandish, weird (but making sense in-universe), funny, or otherwise unexpected from such a serious intent are welcome. For example:

- a plate carrier that's bright-pink
- a gun that has fungus growing out of its metal
- an outfit that emits an otherworldly glow (without actually illuminating its surroundings)
- a common fruit sporting a weird color (without having any health or morale effects otherwise)

### What items go

For higher-amount donations, items may be added into the game.

Without going into spoilers, I have a way to justify odd, unusual, or outright-weird items existing in the game's world. The oddity of suggested items can thus range between out-of-place, ahistorical firearms, to strange tablets in an unknown language, to everyday items made out of strange, living metals, and beyond.

As such, similar suggestions for items are also welcome. The items may be practical (weapons, armor, gear, food, medical supplies...) or decorative (letters in a strange language, a glass box that causes voices to appear in your mind, a banana made out of titanium...). Some limitations may apply, however, based on whether an item is feasible (i.e., if the game allows it to exist) and other potential in-game limitations. Please contact me using the methods described below prior to making a donation if you're not sure if such an item can exist in the game.

### The rules and limitations

The primary goal of these mods is to allow other players to enjoy more out of the same game. As such, I will carefully consider the suggestions of supporters before adding them. Some suggestions may be rejected because they don't follow the rules outlined below. Some may be rejected because it would be too tedious to implement (with my sanity and comfort being an important factor). I wish to be open-minded and diplomatic, so if I find a given suggestion ill-fitting, for one reason or another, I'd prefer to engage in dialogue in order to come up with a satisfactory alternative.

However, under no circumstances any of the following be added to the mods:

- things that insult or diminish the dignity of another person or group of people
- things that promote a group, movement, ideology, idea, brand, or name that seeks to insult or diminish the dignity of another person or group of people
- misinformation, misrepresentation, or falsehoods that seek to harm, exploit, discriminate against, degrade, or otherwise take advantage of a person or group of people
- things that promote or glorify reckless, dangerous, unhealthy, or immoral behavior to self or others
- things that are gross or repulsive on a visceral level
- things of explicit sexual nature that has no artistic, historical, or educational value on its own
- using another person's likeness without their explicit consent

Donations that make these suggestions will be refunded, and no negotiations will take place for an alternative. If you're uncertain whether your suggestion would fit into any of these, please contact me using any of the methods described below prior to making a donation.

The list is non-exhaustive and may be amended at any moment. Your suggestion may be declined even if it doesn't break the rules above. (Yes, this is a very broad power. Legislative battles throughout the ages prove this to be a necessity for someone without an army of lawyers to argue their case, in court or otherwise. Long story short: the sanity and dignity of myself and the people enjoying my mods is by far more valuable than any amount of money.)

## Ways to Contact Me

Feel free to reach out with questions, suggestions, or ideas.

- Discord: `thatfanficguy`
- Email: [frontiermods@protonmail.com](email:frontiermods@protonmail.com)
