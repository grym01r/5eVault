---
player:
level: 3
race: Human
class: Wizard
subclass:
max_hp: 15
ac: 11
spell_dc: 12
proficiency_bonus: 2
status: Active
Connected_Groups:
Connected_Quests:
tags:
  - People
  - Player
---

 > [!infobox|left clean]
> # <span style="font-size:25px">*Bob*</span>
> # <span style="font-size:15px">*Player Name*</span>
> ![[image.png|cover hmedium]]
> ##### Stats
> ```stats
> items:
>   - label: Race
>     value: '{{ frontmatter.race }}'
>   - label: Level
>     value: '{{ frontmatter.level }}'
>   - label: Class
>     value: '{{ frontmatter.class }}'
>   - label: Armor Class
>     value: '{{ frontmatter.ac }}'
>   - label: Initiative
>     value: '+{{ modifier abilities.dexterity }}'
>   - label: Spell DC
>     value: '{{ frontmatter.spell_dc }}'
> grid:
>   columns: 3
> ```
> 
> ##### Abilities
> ```ability
> abilities:
>   strength: 8
>   dexterity: 12
>   constitution: 13
>   intelligence: 15
>   wisdom: 14
>   charisma: 10
> 
> proficiencies:
>   - strength
>   - dexterity
> ```
> 
> ##### Health 
>  ```healthpoints
> state_key: din_health
> health: '{{ frontmatter.max_hp }}'
> death_saves: true
> hitdice:
>   dice: d6
>   value: 3
> ```
>

>[!NOTE|no-title]
>~~~meta-bind
>INPUT[select(
>option(1, ✨Spell Slots),
>option(2, 💪Traits),
>option(3, 🔗Connections),
>option(4, 🎒Inventory),
>option(5, 📝GM Notes),
>class(tabbed)
>)]
>~~~
> >[!tabbed-box]
> > > [!div-m|no-title]
> > > ![[#Spell Slots|no-h clean]]
> >
> > > [!div-m|no-title]
> > > ![[#Traits|no-h1 clean]]
> >
> > > [!div-m|no-title]
> > > ![[#Connections|no-h clean]]
> >
> > > [!div-m|no-title]
> > > ![[#Inventory|no-h1 clean]]
> >
> > > [!div-m|no-title]
> > > ![[#GM Notes|no-h1 clean]]

# Skills

```skills 
proficiencies: 
- insight 
- investigation
  
expertise: 
- investigation 
```

# Spell Slots

```consumable
items:
  - label: "Level 1"
    state_key: din_spells_1
    uses: 4
  - label: "Level 2"
    state_key: din_spell_2
    uses: 2
```

# Traits

### Luck Points
```consumable
label: ""
state_key: din_luck_points
uses: 3
```

You have inexplicable luck that seems to kick in at just the right moment.

**You have 3 luck points.** Whenever you make an attack roll, an ability check, or a saving throw, you can spend one luck point to roll an additional d20. You can choose to spend one of your luck points **after you roll the die, but before the outcome is determined**. You choose which of the d20s is used for the attack roll, ability check, or saving throw.

You can also spend one luck point when an **attack roll** is made against you. Roll a d20 and then choose whether the attack uses the attacker's roll or yours.

If more than one creature spends a luck point to influence the outcome of a roll, the points cancel each other out; no additional dice are rolled.

You regain your expended luck points when you finish a long rest.

### Arcane Recovery
```consumable
label: ""
state_key: din_arcane_recovery
uses: 1
```

You have learned to regain some of your magical energy by studying your spell book. Once per day when you finish a **short rest**, you can choose expended spell slots to recover. The spell slots can have a combined level that is equal to or **less than half your wizard level** (rounded up), and none of the slots can be 6th level or higher.

For example, if you're a 4th-level wizard, you can recover up to two levels worth of spell slots. You can recover either a 2nd-level spell slot or two 1st-level spell slots.

# Connections

Quests: `INPUT[inlineListSuggester(optionQuery(#Quest)):Connected_Quests]`

Groups: `INPUT[inlineListSuggester(optionQuery(#Group)):Connected_Groups]`

# Inventory

#### Ring of Investigation
```consumable
label: ""
state_key: din_items__ring_of_investigation
uses: 3
```

_"May the ability to see also provide you with a clear vision" Grants +1 to Investigation Roles_


# GM Notes