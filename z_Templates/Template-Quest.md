---
Container:
  - "[[z_Templates/World Builder Templates/Template-PointofInterest.md|Template-PointofInterest]]"
  - "[[z_Templates/World Builder Templates/Template-Place.md|Template-Place]]"
  - "[[z_Templates/World Builder Templates/Template-Hub.md|Template-Hub]]"
questObtained:
questStatus: Not Started
questGiver:
questLocationObtained:
questSessionObtained:
questNotes:
questLootAvail:
questLootEarned:
tags:
  - quest
---

> [!NOTE] Parent Region: `INPUT[inlineListSuggester(optionQuery(#Hub),optionQuery(#Region),optionQuery(#Place),optionQuery(#PointofInterest)):Container]`

> [!column|no-i no-t]
>> [!info|no-title] Map
>> Insert Image Here
>
>> [!note|no-title] Town Name
>> ~~~meta-bind
>> INPUT[select(
>> option(1, 🏆Quest Info),
>> option(2, 🕵️‍♀️Quest Details),
>> option(3, 📝GM Notes),
>> class(tabbed)
>> )]
>> ~~~
>>>[!tabbed-box]
>>> >[!div-m|no-title]
>>> > ![[#Quest Info|no-h clean]]
>>>
>>> >[!div-m|no-title]
>>> > ![[#Quest Details|no-h clean]]
>>>
>>> > [!div-m|no-title]
>>> > ![[#GM Notes|no-h clean]]
>>> 


> [!NOTE|no-title] 
> ~~~meta-bind
> INPUT[select(
> option(1, 🏡Backstory),
> option(2, 🍎Planning),
> option(3, 🙎‍♂️People),
> class(tabbed)
> )]
> ~~~
>>[!tabbed-box|div-m]
>>>[!div-m|no-title]
>>> ![[#Backstory|no-h clean]]
>>
>>> [!div-m|no-title]
>>> ![[#Planning|no-h clean]]
>>
>>> [!div-m|no-title]
>>> ![[#People|no-h clean]]



---
# Quest Info

Provide a summary of the quest here. 

- [ ] Obtain the quest
- [ ] Embark on an epic journey
- [ ] Complete the quest
- [ ] Roll in epic loot

# Quest Details


Date Obtained: `INPUT[datePicker:questObtained]` 
Status: `INPUT[inlineSelect(option(Not Started), option(In Progress), option(Complete)):questStatus]` 
Quest Giver: `INPUT[suggester(optionQuery(#Person)):questGiver]` 
Quest Location: `INPUT[suggester(optionQuery(#Hub)):questLocationObtained]` 
Session Obtained: `INPUT[suggester(optionQuery(#Journal)):questSessionObtained]` 
Available Loot: `INPUT[suggester(optionQuery(#item)):questLootAvail]` 
Acquired Loot: `INPUT[suggester(optionQuery(#item)):questLootEarned]` 

# GM Notes

Make notes of what you need to track about the quest here. 

# Backstory

Describe the backstory of the quest here. Why is it important for the party to complete?

# Planning

```ad-flowchart
![[Waterdeep Dragon Heist First Quest|900]]
```

# People

`BUTTON[newNPC]` The following people are associated with this quest.

```dataview
TABLE WITHOUT ID link(file.name) AS "Name", char_race AS "Race", char_gender AS "Gender", Connected_Groups AS "Associated Group"
FROM "1. World Almanac/NPCs"
WHERE contains(char_status, "Alive")
WHERE contains(Connected_Quests, this.file.link)
SORT file.name ASC
```





