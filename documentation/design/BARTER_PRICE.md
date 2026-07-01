# Barter Price Calculation

Frontier Mods uses a very simple system to calculate an item's post-Cataclysm barter value. In short, we use the item's survival utility, storage longevity, and production scarcity to model their trade desirability.

## Barter Price Index

Each of the three parameters mentioned above is provided for each item via the index object, e.g.:

```typescript
{
  price_postapoc: {
    utility: number | ParameterValue,
    longevity: number | ParameterValue,
    scarcity: number | ParameterValue
  }
}
```

The values can be either a number (ranging from 0 to 3) or one of the following `ParameterValue` strings:

* `none` (corresponds to 0)
* `low` (1)
* `medium` (2)
* `high` (3)

Strings are provided for ergonomics and clarity. Internally, they are computed to their respective numerical values, which are then used for calculations.

### Parameters & values

For each parameter, the values mean:

* **utility**:
  * `0` or `none`: no real use; sentimental or purely-decorative items
    * jewelry, postcards, fashion items, make-up, personal items
  * `1` or `low`: comfort or quality-of-life; non-essential items that become useful once all of the basic needs were fulfilled
    * spices, armor, alcohol, coffee, weapons, ammo
  * `2` or `medium`: tools and materials to settle and survive
    * fire, power, house structure, specialized medicine, seeds
  * `3` or `high`: essential survival items
    * food, water, first aid medicine, fuel, clothing, basic tools

* **longevity**:
  * `0` or `none`: extremely-short lifespan; either fragile or quickly-perishible
    * dairy, Christmas baubles, bread
  * `1` or `low`: useful for some time; things that last for days or a few weeks
    * non-rechargeable batteries, fresh produce, open fuel
  * `2` or `medium`: long-lasting; able to withstand use or storage for weeks or months
    * canned foods, common clothing, rechargeable batteries
  * `3` or `high`: extremely-long lifespan; items that last several years or more, or can withstand heavy use
    * metal tools, ammo, freeze-dried foods, sealed medication

* **scarcity**:
  * `0` or `none`: everpresent; easy to obtain without any effort, either through casual search or unskilled production using minimal commonplace materials
    * wooden branches, snowballs, rocks
  * `1` or `low`: easily found or made with some effort or skill
    * wooden furniture, basic weapons
  * `2` or `medium`: requires specialized tooling and/or skill to manufacture
    * woven textiles, basic reusable tools
  * `3` or `high`: impossible to manufacture anymore
    * antibiotics, specialized tools, refined materials, precision electronics
    
The computed value of the index (the sum of its three values, ranging from 0 to 9) is applied to the Fibonacci sequence, with the start of the sequence offset by 2. The number at the index within the sequences is multiplied by 50 cents to produce the resulting barter value. This makes most items valuable but not exceptional, and highly-sought-after items valued as such.

### Quick Lookup Table

| Index | Fibonacci | Barter value |
|-------|-----------|--------------|
| 0     | 1         | $0.50        |
| 1     | 2         | $1.00        |
| 2     | 3         | $1.50        |
| 3     | 5         | $2.50        |
| 4     | 8         | $4.00        |
| 5     | 13        | $6.50        |
| 6     | 21        | $10.50       |
| 7     | 34        | $17.00       |
| 8     | 55        | $27.50       |
| 9     | 89        | $44.50       |
