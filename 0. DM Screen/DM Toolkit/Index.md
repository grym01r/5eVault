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

# Subclasses
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
# Races
```base
views:
  - type: cards
    name: Races
    filters:
      and:
        - file.tags.contains("race")
    order:
      - aliases
    image: note.image
    cardSize: 650
    imageAspectRatio: 0.6
    imageFit: contain

```
# Backgrounds
```base
views:
  - type: cards
    name: Backgrounds
    filters:
      and:
        - file.tags.contains("background")
    order:
      - aliases
    image: note.image
    cardSize: 540
    imageAspectRatio: 0.4

```