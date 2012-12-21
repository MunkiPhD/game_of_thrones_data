#game_of_thrones_data?#
###SPOLER ALERT!!!###
By looking at the data you will see information that may give hints to certain plot twists in the story up through the fifth book (A Dance with Dragons).
##Description##
**game_of_thrones_data** is a compilation of data based on the series of novels A Song of Ice and Fire - better known by the HBO series, **Game of Thrones**.

Since the data is based on fictional characters and areas with backstories and relationships,
it is much easier to create meaningful test data for your application.

For example, if you were creating a team based pvp game, you could generate the data like:

- ***Cersei*** is on team ***Lannister***
- ***Eddard*** is on team ***Winterfell***
- ***Lannister*** vs ***Wintefell*** played at stadium ***King's Landing***

As a result, data is understand since you can use the story to guide use cases. it makes more sense than:
* **TeamRed** *played* **TeamBlue** or
* **Player1** *killed* **Player2**

It can also help find bugs if you were to find something such as:
- **Tyrion** *killed* **Tywin**

as that would not happen since they are both on ***Team Lannister***

##Schema##
=======
* people
  * dob: Date of Birth (normalized to 20 and 21st century time)
  * sex: male or female, represented as "m" or "f"
  * email: a fictional email address that might belong to this character
  * titles[]: important titles that character has held [lord, squire, king, hand of the king, etc]
  * nickname: Person's nickname (e.g. "Kingslayer")
  * aid: arbitrary ID assigned to this person that can be used for reference
  * house_id: the ID of the house this person belongs to (might need to distinguish the difference between  ***from*** and ***currently at*** e.g. Catelyn Stark is from Tully, but is at Stark)
* houses
    * house name
      * sigil: A description of the house's sigil (e.g. Direwolf for house Stark)
      * colors[]: an array of the colors of the house (e.g. crimson and gold for house Lannister)
      * seat: The seat held by the house (e.g. the king sits the iron throne, house Tully sits Riverrun)
      * motto: The motto/saying of the house, official or unnofficial (e.g. Lannister's "Hear me roar!")
      * aid: arbitrary ID assigned to the house that can be used for reference
* orders
  * order name (e.g. Kingsguard, Night's Watch)
    * colors[]: the colors of the order (e.g. Black for the Night's Watch)
    * motto: the motto of the order
    * aid: arbitrary ID assigned to the order that can be used for reference
* castles
  * name: the name of the castle
  * ruined: whether the castle is a ruined castle

###Loading the data###
The data was created using [yaml_db](https://github.com/ludicast/yaml_db). You can read the documentation for loading the data into your database, especially if you have a Rails app.

##License##
###Permissions###
Completely open permissions. Fork it, expand it, etc. If you have updates to the data, issue a pull request and it will be merged in after it's been reviewed.
The data is meant to be a starting point for generating data for your app in an easy manner - as a service for the commnunity as fans of both the novels, the show, and FOSS.

###Plans###
Create configurable data seed scripts for importing into various platforms (e.g. Rails using Devise)
