# README #

> This is repo that contains Warframe.market item database in JSON format.

> Icon files is not included in that repo.

> How to contribute icons, read bellow.

## Item Template ##

This is an **example** with all possible fields:

```
#!json

{
  "_id": "54a73e65e779893a797fff22",
  "tradable": true,
  "patched": true,
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
  "ducats": "15",
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

![Tags](https://lh6.googleusercontent.com/jtvaa3dCbMJAi1GEtUHaHunD_pxGgG9VdLQsaQo0GEmwjc6uMa9d4EspZjC6n9kLjKYzFg9NGfGkAQA=w1920-h1083-rw)

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


Also, if locale-section contain `icon` field, original icon will be replaced with icon from locale-section.

This is mostly for mods.