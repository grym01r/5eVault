
```base
type: table
views:
  - type: table
    name: Search
    filters:
      and:
        - file.name.contains("action")
        - file.tags.contains("rule")
    order:
      - file.name
      - file.tags
    sort:
      - property: obsidianUIMode
        direction: ASC
      - property: benefits
        direction: ASC
      - property: author
        direction: ASC
      - property: alias
        direction: ASC
    limit: 10
    columnSize:
      file.name: 274

```

# Damage
| Name             | Effect                              |
| ---------------- | ----------------------------------- |
| Resistance       | 1/2 dmg                             |
| Immunity         | 0 damage                            |
| Vulnerable       | x2 damage                           |
| Obscured         | Disadvantage                        |
| Lightly Obscured | Disadvantage on Wisdom (Perception) |

# Cover
| Degree      | Effect                                                                                                         |
| ----------- | -------------------------------------------------------------------------------------------------------------- |
| Half Cover  | +2 bonus to AC and Dex Saving throws                                                                           |
| 3/4 Cover   | +5 bonus to AC and Dex Saving throws                                                                           |
| Total Cover | Cannot be targeted directly by attacks or spells, although area of effect spells and abilities still effective |

# Donning & Doffing Armor
| Category | Don      | Doff     |
| -------- | -------- | -------- |
| Light    | 1 min    | 1 min    |
| Medium   | 5 min    | 1 min    |
| Heavy    | 10 min   | 5 min    |
| Shield   | 1 action | 1 action | 

# Exhaustion

![[0. DM Screen/books/dungeon-masters-guide-2024/02-chapter-2-running-the-game.md#Extended Travel]]

| Level | Effect                                         |
| ----- | ---------------------------------------------- |
| 1     | Disadvantage on ability checks                 |
| 2     | Speed halved                                   |
| 3     | Disadvantage on attack rolls and saving throws |
| 4     | Hit point maximum halved                       |
| 5     | Speed reduced to 0                             |
| 6     | Death                                          | 

# Lifestyle Expenses
| Lifestyle    | Price/day     |
| ------------ | ------------- |
| Wretched     | -             |
| Squalid      | 1 sp          |
| Poor         | 2 sp          |
| Modest       | 1 gp          |
| Comfortable  | 2 gp          |
| Wealthy      | 4 gp          |
| Aristocratic | 10 gp minimum | 

> [!info]- Character Creation
> [[Index#Classes|Classes]]
> [[Index#Subclasses|Subclasses]]
> [[Index#Races|Races]]
> [[Index#Backgrounds|Backgrounds]]

> [!info]- Conditions
> [[Conditions#Blinded|Blinded]]
> [[Conditions#Charmed|Charmed]]
> [[Conditions#Concentration|Concentration]]
> [[Conditions#Dazed|Dazed]]
> [[Conditions#Deafened|Deafened]]
> [[Conditions#Exhaustion|Exhaustion]]
> [[Conditions#Flanked|Flanked]]
> [[Conditions#Frightened|Frightened]]
> [[Conditions#Grappled|Grappled]]
> [[Conditions#Incapacitated|Incapacitated]]
> [[Conditions#Invisible|Invisible]]
> [[Conditions#Paralyzed|Paralyzed]]
> [[Conditions#Petrified|Petrified]]
> [[Conditions#Poisoned|Poisoned]]
> [[Conditions#Prone|Prone]]
> [[Conditions#Restrained|Restrained]]
> [[Conditions#Stunned|Stunned]]
> [[Conditions#Unconscious|Unconscious]]

> [!info]- Combat Actions
> [[actions#Actions#Activate Item|Activate Item]]
> [[actions#Actions#Attack|Attack]]
> [[actions#Actions#Magic|Cast a Spell]]
> [[actions#Actions#Dash|Dash]]
> [[actions#Actions#Disengage|Disengage]]
> [[actions#Actions#Disarm|Disarm]]
> [[actions#Actions#Dodge|Dodge]]
> [[actions#Actions#Escape a Grapple|Escape a Grapple]]
> [[actions#Actions#Unarmed Strike#Grapple|Grapple]]
> [[actions#Actions#Help|Help]]
> [[actions#Actions#Hide|Hide]]
> [[actions#Actions#Opportunity Attack|Opportunity Attack]]
> [[actions#Actions#Overrun|Overrun]]
> [[actions#Actions#Ready|Ready]]
> [[actions#Actions#Search|Search]]
> [[actions#Actions#Unarmed Strike#Shove|Shove]]
> [[actions#Actions#Tumble|Tumble]]
> [[actions#Actions#Unarmed Strike|Unarmed Strike]]
> [[actions#Actions#Utilize|Utilize]]


> [!info]- Misc. Combat
> [[0. DM Screen/books/players-handbook-2024/02-chapter-1-playing-the-game.md#Surprise|Surprise]]
> [[0. DM Screen/variant-rules/initiative-xphb.md|Initiative]]
> [[0. DM Screen/variant-rules/reaction-xphb.md|Reactions]]
> [[actions#Actions#Two-Weapon Fighting|Two-Weapon Fighting]]
> [[0. DM Screen/variant-rules/improvised-weapons-xphb.md|Improvised Weapons]]
> [[conditions#Prone|Being Prone]]
> [[10-combat#Ranged Attacks in Close Combat|Ranged Attacks in Close Combat]]
> [[10-combat#Mounted Combat|Mounted Combat]]

> [!info]- Movement
> [[0. DM Screen/variant-rules/difficult-terrain-xphb.md|Difficult Terrain]]
> [[0. DM Screen/books/dungeon-masters-guide-2024/02-chapter-2-running-the-game.md#Travel Pace|Travel Pace]]
> [[0. DM Screen/books/dungeon-masters-guide-2024/02-chapter-2-running-the-game.md#Extended Travel|Forced March]]
> [[0. DM Screen/books/dungeon-masters-guide-2024/02-chapter-2-running-the-game.md#Vehicles|Mounts and Vehicles]]
> [[0. DM Screen/variant-rules/swimming-xphb.md|Swimming]]
> [[0. DM Screen/variant-rules/jumping-xphb.md|Jumping]]
> [[0. DM Screen/variant-rules/crawling-xphb.md|Crawling]]
> [[0. DM Screen/books/dungeon-masters-guide-2024/02-chapter-2-running-the-game.md#Navigation|Navigation]]
> [[0. DM Screen/books/dungeon-masters-guide-2024/02-chapter-2-running-the-game.md#Foraging|Foraging]]
> Activity while Traveling

> [!info]- Resting
> [[0. DM Screen/tables/food-drink-and-lodging-xphb.md|Food, Drink, and Lodging]]
> [[0. DM Screen/variant-rules/short-rest-xphb.md|Short Rest]]
> [[0. DM Screen/variant-rules/long-rest-xphb.md|Long Rest]]
> [[malnutrition-xphb|Malnutrition]]
> [[dehydration-xphb|Dehydration]]

> [!info]- Healing and Death
> [[0. DM Screen/books/players-handbook-2024/02-chapter-1-playing-the-game.md#Healing|Healing]]
> [[0. DM Screen/books/players-handbook-2024/02-chapter-1-playing-the-game.md#Instant Death|Instant Death]]
> [[0. DM Screen/books/players-handbook-2024/02-chapter-1-playing-the-game.md#Falling Unconscious|Falling Unconscious]]
> [[0. DM Screen/books/players-handbook-2024/02-chapter-1-playing-the-game.md#Death Saving Throws|Death Saving Throws]]
> [[0. DM Screen/books/players-handbook-2024/02-chapter-1-playing-the-game.md#Stabilizing a Creature|Stabilizing a Creature]]
> [[0. DM Screen/books/players-handbook-2024/02-chapter-1-playing-the-game.md#Monsters and Death|Monsters and Death]]

> [!info]- Weapons and Armor
> [[0. DM Screen/tables/weapons-xphb.md|Weapons]]
> [[0. DM Screen/tables/armor-xphb.md|Armor and Shields]]

>[!info]- Magic
>**Spell Save DC**
> 8 + magic ability modifier + proficiency bonus 
> 
> **Spell Attack Modifier**
> Proficiency + ability mod
> 
> **Identifying Magic Items**
> - Holding an item makes you sense magic
> - Identify spell to reveal its properties
> - Long rest and concentration to reveal properties
>
>**Attuning**
>Requires an uninterrupted short rest with concentration in the form of prayers, weapon practice, or meditation. You can attune no more than 3 items.

> [!info]- Skills
> [[Skills#Acrobatics|Acrobatics]]
> [[Skills#Animal Handling|Animal Handling]]
> [[Skills#Arcana|Arcana]]
> [[Skills#Athletics|Athletics]]
> [[Skills#Deception|Deception]]
> [[Skills#History|History]]
> [[Skills#Insight|Insight]]
> [[Skills#Intimidation|Intimidation]]
> [[Skills#Investigation|Investigation]]
> [[Skills#Medicine|Medicine]]
> [[Skills#Nature|Nature]]
> [[Skills#Perception|Perception]]
> [[Skills#Performance|Performance]]
> [[Skills#Persuasion|Persuasion]]
> [[Skills#Religion|Religion]]
> [[Skills#Sleight of Hand|Sleight of Hand]]
> [[Skills#Stealth|Stealth]]
> [[Skills#Survival|Survival]]

>[!info]- Treasure
>[[treasure-xdmg|Treasure]]
>[[25-gp-art-objects-xdmg|25 GP Art Objects]]
>[[250-gp-art-objects-xdmg|250 GP Art Objects]]
>[[750-gp-art-objects-xdmg|750 GP Art Objects]]
>[[2500-gp-art-objects-xdmg|2,500 GP Art Objects]]
>>[!info]- Common Magic Items
>> [[arcana-common-xdmg|Arcana - Common]]
>> [[armaments-common-xdmg|Armaments - Common]]
>> [[implements-common-xdmg|Implements - Common]]
>> [[relics-common-xdmg|Relics - Common]]
>
>>[!info]- Uncommon Magic Items
>> [[arcana-uncommon-xdmg|Arcana - Uncommon]]
>> [[armaments-uncommon-xdmg|Armaments - Uncommon]]
>> [[implements-uncommon-xdmg|Implements - Uncommon]]
>> [[relics-uncommon-xdmg|Relics - Uncommon]]
>
>> [!info]- Rare Magic Items
>> [[arcana-rare-xdmg|Arcana - Rare]]
>> [[armaments-rare-xdmg|Armaments - Rare]]
>> [[implements-rare-xdmg|Implements - Rare]]
>> [[relics-rare-xdmg|Relics - Rare]]