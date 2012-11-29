#got_data?#
###SPOLER ALERT!!!###
By looking at the data you will see information that may give hints to certain plot twists in the story up through the fifth book (A Dance with Dragons).
##Description##
**got_data** (or **GoT_data**, see what I did there? *+1 for wit*) is a compilation of data based on the series of novels A Song of Ice and Fire - better known by the HBO series, **Game of Thrones**.

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
  * sex: male or female
  * email: a fictional email address that might belong to this character
  * titles[]: important titles that character has held [lord, squire, king, hand of the king, etc]
  * nickname: Person's nickname (e.g. "Kingslayer")
* houses
    * house name
      * sigil: A description of the house's sigil (e.g. Direwolf for house Stark)
      * colors[]: an array of the colors of the house (e.g. crimson and gold for house Lannister)
      * seat: The seat held by the house (e.g. the king sits the iron throne, house Tully sits Riverrun)
      * motto: The motto/saying of the house, official or unnofficial (e.g. Lannister's "Hear me roar!")
* orders
  * order name (e.g. Kingsguard, Night's Watch)
    * colors[]: the colors of the order (e.g. Black for the Night's Watch)
    * motto: the motto of the order

##License##
###Permissions###
Completely open permissions. Fork it, expand it, etc. If you have updates to the data, issue a pull request and it will be merged in after it's been reviewed.
The data is meant to be a starting point for generating data for your app in an easy manner - as a service for the commnunity as fans of both the novels, the show, and FOSS.

###Plans###
Create configurable data seed scripts for importing into various platforms (e.g. Rails using Devise)
