got_data?
========

got_data (or GoT_data, see what I did there? +1 for wit)
A compilation of data based on the series of novels A Song of Fire and Ice - better known by the HBO series, Game of Thrones.

Since the data is based on fictional characters and areas, it is much easier to create test data that has actual meaning to the person testing or developing.

For example, if you were creating a team based pvp game, you could generate the data like:

*Cersei* is on team *Lannister*
*Eddard* is on team *Winterfell*
*Lannister* vs *Wintefell* played at stadium *King's Landing*

There are varios collections of data. At the moment they are structured as such:

people
  dob: Date of Birth (normalized to 20 and 21st century time)
  sex: male or female
  email: a fictional email address
  titles[]: titles that person has held [lord, squire, king, hand of the king, etc]

houses
  house name
    banner: the representation of the house (e.g. Direwolf for house Stark)
    colors[]: an array of the colors of the house (e.g. crimson and gold for house Lannister)
    seat: The seat held by the house (e.g. the king sits the iron throne, house Tully sits Riverrun)
    motto: the motto of the house (e.g. "A Lannister always pays his debts")
     
orders
  name of the order (e.g. Kingsguard, Night's Watch)
    colors[]: the colors of the order (e.g. Black for the Night's Watch)
    motto: the motto of the order

