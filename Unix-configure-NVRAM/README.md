###################################
#        IDPROM INVALID           #
###################################

# Example MAC-ADD : 00:00:00:31:82:20 /0:3:ba:31:82:20 / 08:00:20:31:82:20
# Ultra MAC Address 08:00:20:HOSTID
# Sun Blade 150 MAC Address 08:00:20:HOSTID / 00:03:ba:HOSTID / 00:00:00:HOSTID


press stop + a 
ok show-devs 
ok cd /pci@1f,0/ebus@c/eeprom@1,0 
ok .properties 
ok <device address> >physical 
ok showstack 
ok 2000 memmap 
ok 1fd0 +
ok 30 dump 
ok 01 <Address value>d8 c! 
# Address value : take 6 digits only + d8 c! 

ok <80 or 83> <Address value>d9 c! 
# 80 : machine type sun ultra 
# 83 : machine type sunblade 

MAC Address : 08-00-20-31-82-20
ok <first letter MAC address> <Address value>da c! 
ok <second letter MAC address> <Address value>db c! 
ok <third letter MAC address> <Address value>dc c! 
ok <fourth letter MAC address> <Address value>dd c! 
ok <fifth letter MAC address> <Address value>de c! 
ok <sixth letter MAC address> <Address value>df c! 

Write 00 (if not already) for production date : 
ok 00 <Address value>e0 c! 
ok 00 <Address value>e1 c! 
ok 00 <Address value>e2 c! 
ok 00 <Address value>e3 c! 

Write host ID (Three last letters MAC Address) 
ok <host ID> <Address value>e4 c! 
ok <host ID> <Address value>e5 c! 
ok <host ID> <Address value>e6 c! 

Calculate XOR-Checksum value starting d8-e6 (except e0-e3)
ok <d8> <d9> xor 
ok <da> xor 
ok <db> xor 
ok <dc> xor 
ok <dd> xor 
ok <de> xor 
ok <df> xor 
ok <e4> xor
ok <e5> xor 
ok <e6> xor 

Calculate checksum
ok <value beside the prompt> <Address value>e7 c!

ok banner
ok reset-all
