# README #

> This is repo that contains Warframe.market item database in JSON format.

> Icon files is not included in that repo.

> How to contribute icons, read bellow.

## Directories ##

`updates` - all singular changes belongs to this dir.

If some item need to be updated\added, just create file, like `%item_name%.json`

Then, that item will be verified and if all its fields is correct, it will be added into db and then removed from this directory.

If some of the fields isn't correct, item will be added into db, but will stay present in that directory.



`examples` - some examples =)

## Item Template ##

This is an **example** with all possible fields:

```
#!json

{
  "_id": "54a73e65e779893a797fff22",
  "tradable": true,
  "url_name": "akbronco_prime_blueprint",

  "icon_format": "land",
  "icon": "icons/en/Akbronco_Prime_Set.34b5a7f99e5f8c15cc2039a76c725069.png",
  "thumb": "icons/en/thumbs/Akbronco_Prime_Set.34b5a7f99e5f8c15cc2039a76c725069.128x128.png",
  "sub_icon": "sub_icons/blueprint_128x128.png",
  
  "set_root": false,
  "part_of_set": [
    "56783f24cbfa8f0432dd898d",
    "54a73e65e779893a797fff22",
    "54a73e65e779893a797fff23"
  ],

  "tags": [
    "blueprint",
    "prime"
  ],

  "mastery_level": 0,
  "trading_tax": 2000,
  "ducats": 15,
  "mod_max_rank": 0,
  "rarity": "rare",

  "en": {
    "wiki_link": "http://warframe.wikia.com/wiki/Akbronco_Prime",
    "item_name": "Akbronco Prime Blueprint",
    "codex": "Used together, these Orokin pistols feed off each other, inflicting greater damage with an enhanced chance for inducing elemental effects on targets",
    "description": "<p>The Akbronco Prime lowers  Impact damage to increase  Slash damage, while gaining increased firing rate, critical damage, status chance and magazine size. The Akbronco Prime was added into the game in Update 12.4.</p>",
    "drop": [
      {
        "link": null,
        "name": "Lith S2 Common"
      },
      {
        "link": null,
        "name": "Lith S3 Common"
      }
    ]        
  },
  "ru": {
    "wiki_link": "http://ru.warframe.wikia.com/wiki/%D0%90%D0%BA%D0%B1%D1%80%D0%BE%D0%BD%D0%BA%D0%BE_%D0%BF%D1%80%D0%B0%D0%B9%D0%BC/Прайм",
    "item_name": "Акбронко прайм Чертеж",
    "description": "<p>Используемые в паре, эти пистолеты Орокин дополняют друг друга, нанося высокий урон с увеличенным шансом наложения элементального эффекта.</p>",
    "icon": "icons/en/Akbronco_Prime_Set.34b5a7f99e5f8c15cc2039a76c725069.png",
    "thumb": "icons/en/thumbs/Akbronco_Prime_Set.34b5a7f99e5f8c15cc2039a76c725069.128x128.png",
    "drop": [
      {
        "link": null,
        "name": "Lith S2 Common"
      },
      {
        "link": null,
        "name": "Lith S3 Common"
      }
    ]
  }
}
```
## Explanation ##

Most of fields is self-explained.

### Sets ###
 
Is this item a set itself, like "Akbronco Prime Set":

```
#!

"set_root": true\false

```

Which parts present in this set:

```
#!

"part_of_set": [list of ids]
```

*****

### Tags ###

The purpose of tags -> providing a quick-filters:

![Screenshot from 2016-10-31 18-00-12.png](https://bitbucket.org/repo/8EAodE/images/349767049-Screenshot%20from%202016-10-31%2018-00-12.png)

Requirenments:

* Be a lowercase
* Without spaces, replace spaces with `_`:
* No special characters

Because, tags are used in lang-files as base string for translation.(frontend)

*****

### Drop ###

`name` - Just a name of NPC\location

`link` - Link to external site, like **wiki**. Or link to internal location, like **Axi N3 Relic**

*****

### Other Languages ###

If you wanna add another language support.

Just copy "en"\"ru" section, and replicate it with correct translations.

All missed fields will be ignored.

*****

### Icon ###

If you wanna contribute an icon.

Add a `remote://` prefix to external-url, like:

```
#!

remote://http://vignette3.wikia.nocookie.net/warframe/images/3/30/AssimilateMod.png/revision/latest?cb=20160831214533
```


Also, any locale-section can contain `icon` field, you know, en-icon will be displayed for en-language, ru-icon for ru, etc.

This is mostly for mods.

## Relics ##

In case that new relics were added or need to be updated.

**Do not** create all 4 types of one relic [innact, Exceptional, ... etc]

Create only one instance that contains its name, like: `Meso V3`

All variations will be formed by the script.