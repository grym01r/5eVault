---
aliases:
Category:
Container:
tags:
  - place
---

> [!NOTE] Parent Hub: `INPUT[suggester(optionQuery(#Hub)):Container]`

> [!column|no-title]
>> [!note|no-title]
>> ![[#Image|no-h clean]]
>
>> [!note|no-title] Place Name
>> ~~~meta-bind
>> INPUT[select(
>> option(1, ℹ️General Info),
>> option(2, 🏃‍♂️‍➡️NPCs),
>> option(3, 📝GM Notes),
>> class(tabbed)
>> )]
>> ~~~
>>>[!tabbed-box]
>>> >[!div-m|no-title]
>>> > ![[#General|no-h clean]]
>>>
>>> >[!div-m|no-title]
>>> > ![[#NPCs|no-h clean]]
>>>
>>> > [!div-m|no-title]
>>> > ![[#GM Notes|no-h clean]]
>>> 

> [!NOTE|no-title]
> ~~~meta-bind
> INPUT[select(
> option(1, 🛒Selling),
> option(2, 🪙Buying),
> option(3, 🛠️Services),
> option(4, 🤐Rumours),
> class(tabbed)
> )]
> ~~~
> >[!tabbed-box]
> > >[!div-m|no-title]
> > > ![[#Selling|no-h clean]]
> >
> > > [!div-m|no-title]
> > > ![[#Buying|no-h clean]]
> > 
> > > [!div-m|no-title]
> > > ![[#Services|no-h clean]]
> > 
> > > [!div-m|no-title]
> > > ![[#Rumours|no-h clean]]

---

# General

Select Settlement: `INPUT[suggester(optionQuery(#Hub)):Container]`

Select Category: `INPUT[inlineSelect(option(Commerce), option(Agriculture), option(Military), option(Philosophy), option(Industrial), option(Nesting), option(Government)):Category]`

This is the places description. 

# NPCs

`BUTTON[newNPC]` The following people are associated with this place.

```dataview
TABLE WITHOUT ID link(file.name) AS "Name", char_race AS "Race", char_gender AS "Gender"
FROM "1. World Almanac/NPCs"
WHERE contains(char_status, "Alive")
WHERE contains(Container, this.file.link)
SORT file.name ASC
```

# GM Notes

Make notes of what you need to track in the town here. 


# Selling

The following items are available for purchase. 

```dataviewjs
// ---- CONFIG ---------------------------------------------------

// Exclude these rarities (case-insensitive):
const excludedRarities = ["legendary", "very rare"];

// Optional: filter by item types (leave empty for "any type")
const allowedTypes = [];   // e.g., ["weapon", "armor"]

// Number of random items to pick:
const count = 3;

// ---------------------------------------------------------------

// normalize function (case-insensitive comparison)
const norm = s => (typeof s === "string" ? s.toLowerCase().trim() : "");

// get all items
let all = dv.pages('"2. Compendium/Items"').values;

// 1. Filter out excluded rarities
let filtered = all.filter(p => {
  let rarity = norm(p.rarity ?? "");
  return !excludedRarities.map(norm).includes(rarity);
});

// 2. If item types are specified, apply that filter too
if (allowedTypes.length > 0) {
  filtered = filtered.filter(p => {
    let type = p["item type"];
    if (Array.isArray(type))
      return type.map(norm).some(t => allowedTypes.map(norm).includes(t));
    return allowedTypes.map(norm).includes(norm(type));
  });
}

// 3. Shuffle (Fisher–Yates)
for (let i = filtered.length - 1; i > 0; i--) {
  const j = Math.floor(Math.random() * (i + 1));
  [filtered[i], filtered[j]] = [filtered[j], filtered[i]];
}

// 4. Pick the first N items
let picks = filtered.slice(0, count);

// 5. Render table
dv.table(
  ["Item", "Rarity", "Cost", "Weight"],
  picks.map(p => [
    dv.fileLink(p.file.path),
    p.rarity ?? "—",
    p.value ?? "—",
    p.weight_lb ?? "—"
  ])
);
```

# Buying

List of things this merchant will purchase. 

| Item   | Cost | Weight |
| ------ | ---- | ------ |
| Item 1 | 1gp  | L      |
| Item 2 | 1cp  | -      |

# Services

Services offered. 

| Item   | Cost | Weight |
| ------ | ---- | ------ |
| Service 1 | 1gp  | L      |
| Service 2 | 1cp  | -      |

# Rumours

Anything the party might over hear?

# Image
![[Pasted image 20250425220102.png|500]]

