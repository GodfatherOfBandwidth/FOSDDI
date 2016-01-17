a single table for all DHCPv4 subnet declearations

separate table for DHCPv6 subnets

how many columns can a table have and still be performant?

	chosing table keys and other such features could become very important if the subnet table
	becomes large or the server is low on resources.

different ways to store DHCP options,
	
	as a single field that contains ALL options
	
		easiest, but just doesn't FEEL right ... feels lazy and too easy for errors to creep in.
	
	separate all options into individual columns
	
		this could get very messy as most options have at least 4 sub items that must be present
	
	perhaps a second table that has all the standard options then you could just reference 
	the option number in that table with the correct value and when the config engine returns
	the options it can construct the options correctly from the info in the options table
	and the info from the subnet row in the subnets table
	
		Added bonus of this method is that custom atributes could be added very easily ... I like this : )
