# Party
```base
views:
  - type: cards
    name: Party
    filters:
      and:
        - file.tags.contains("Player")
        - and:
            - '!file.path.contains("z_Templates")'
    order:
      - file.name
      - player
      - level
      - class
      - race
      - max_hp
      - ac
    columnSize:
      file.name: 149
      note.player: 101
      note.level: 75
      note.class: 134
      note.race: 85
      note.max_hp: 91
      note.ac: 86

```


# Session Journals
```base
views:
  - type: table
    name: Session Journals
    filters:
      and:
        - file.tags.contains("journal")
        - '!file.path.contains("z_Templates")'
    order:
      - file.name
      - file.ctime
    columnSize:
      file.name: 300

```

# Create New

#### Player Elements 

`BUTTON[newPC]`

`BUTTON[newJournal]`

#### World Elements

`BUTTON[newNPC]`

`BUTTON[button_group]`

`BUTTON[button_quest]`

`BUTTON[button_region]`

`BUTTON[newHub]`

`BUTTON[button_place]`

`BUTTON[button_pointofinterest]`

# Recently Modified
```base
"0":
  type: table
  name: Recently Modified - All
views:
  - type: table
    name: Table
    order:
      - file.name
      - file.tags
      - file.ctime
      - file.mtime
    sort:
      - property: file.mtime
        direction: DESC
    limit: 20
    columnSize:
      file.name: 285
      file.ctime: 246

```

# Search

```base
type: table
views:
  - type: table
    name: Spells
    filters:
      and:
        - file.tags.contains("spell")
        - file.name.contains("fire")
    order:
      - level
      - aliases
      - file.name
      - concentration
      - spell_slot_upgrade
      - duration
      - components
      - file.tags
    sort:
      - property: aliases
        direction: ASC
      - property: file.tags
        direction: DESC
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
      note.level: 65
      note.aliases: 271
      file.name: 294
      note.concentration: 132
      note.duration: 177
      note.components: 160

```

<br>

```base
type: table
views:
  - type: table
    name: Monsters
    filters:
      and:
        - file.tags.contains("monster")
        - file.name.contains("fire")
    order:
      - aliases
      - file.name
      - cr
      - environment
      - creature type
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
      note.aliases: 223
      file.name: 273
      note.environment: 451
      note.creature type: 199

```

<br>

```base
type: table
views:
  - type: table
    name: Items
    filters:
      and:
        - file.tags.contains("item")
        - file.name.contains("fire")
    order:
      - aliases
      - file.name
      - item type
      - rarity
      - value
      - weight_lb
      - attunement
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
    columnSize:
      note.aliases: 223
      file.name: 273
      note.item type: 132
      note.value: 100
      note.weight_lb: 102

```

<br>

```base
type: table
views:
  - type: table
    name: Feats
    filters:
      and:
        - file.tags.contains("feat")
        - feat_type == "Origin"
    order:
      - aliases
      - file.name
      - feat_type
      - prequisite
      - level
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
      note.aliases: 223
      file.name: 273
      note.prequisite: 357
      note.level: 119

```

<br>

```base
type: table
views:
  - type: table
    name: Rules
    filters:
      and:
        - file.tags.contains("rule")
        - file.name.contains("ability")
    order:
      - aliases
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
    limit: 7
    columnSize:
      note.aliases: 348
      file.name: 556

```

# Classes 
```base
views:
  - type: cards
    name: Classes
    filters:
      and:
        - file.tags.contains("class")
    order:
      - aliases
    image: note.image
    cardSize: 220
    imageAspectRatio: 1.35

```

```base
views:
  - type: cards
    name: Subclasses
    filters:
      and:
        - file.tags.contains("subclass")
    order:
      - aliases
      - parent class
    image: note.image
    cardSize: 230
    imageAspectRatio: 2
    imageFit: ""

```