---
Container:
Category:
tags:
  - region
---

> [!NOTE] Parent Plane: `INPUT[suggester(optionQuery(#World)):Container]`

> [!column|no-i no-t]
>> [!info|no-title] Map
>> Insert Image Here
>
>> [!note|no-title] Town Name
>> ~~~meta-bind
>> INPUT[select(
>> option(1, ℹ️General Info),
>> option(2, 🌐Region Details),
>> option(3, 📝GM Notes),
>> class(tabbed)
>> )]
>> ~~~
>>>[!tabbed-box]
>>> >[!div-m|no-title]
>>> > ![[#General Info|no-h clean]]
>>>
>>> >[!div-m|no-title]
>>> > ![[#Region Details|no-h clean]]
>>>
>>> > [!div-m|no-title]
>>> > ![[#GM Notes|no-h clean]]
>>> 

> [!NOTE|no-title]
> ~~~meta-bind
> INPUT[select(
> option(1, 🏡Hubs),
> option(2, 🍎Points of Interest),
> option(3, ⚔️Groups),
> option(4, 💭Quests),
> class(tabbed)
> )]
> ~~~
> >[!tabbed-box]
> > >[!div-m|no-title]
> > > ![[#Hubs|no-h clean]]
> >
> > > [!div-m|no-title]
> > > ![[#Points of Interest|no-h clean]]
> > 
> > > [!div-m|no-title]
> > > ![[#Groups|no-h clean]]
> > 
> > > [!div-m|no-title]
> > > ![[#Quests|no-h clean]]

---
# General Info

This is the region description. 

# Region Details

**Dominant Races:**  
**Climate:** 
**Seasons:**

# GM Notes

Make notes of what you need to track in the region here. 

# Hubs

`BUTTON[newHub]` Places where people live - Cities, Towns, Villages, Hamlets, Encampment, Keeps, Fortresses, Strongholds.

```dataview
TABLE WITHOUT ID link(file.name) AS "Hubs(s)", MyCategory as "Type"
FROM "1. World Almanac/Locations/Hubs"
WHERE contains(MyContainer, this.file.link)
SORT file.name ASC
```

# Points of Interest

`BUTTON[button_pointofinterest]`  Places that can be explored. 

```dataview
TABLE WITHOUT ID link(file.name) AS "Points of Interest(s)", Category as "Type"
FROM "1. World Almanac/Locations/POIs"
WHERE contains(MyContainer, this.file.link)
SORT file.name ASC
```

# Groups

`BUTTON[button_group]` Groups of people and power - religious, cults, guilds, military.

```dataview
TABLE WITHOUT ID link(file.name) AS "Group(s)", Category as "Type"
FROM "1. World Almanac/Factions"
WHERE contains(MyContainer, this.file.link)
SORT file.name ASC
```


# Quests

`BUTTON[button_quest]` Expeditions or undertakings.

```dataview
TABLE WITHOUT ID link(file.name) AS "Quest(s)", questGiver AS "Quest Giver", questStatus AS "Status"
FROM "3. Quests"
WHERE contains(MyContainer, this.file.link)
SORT file.name ASC
```

