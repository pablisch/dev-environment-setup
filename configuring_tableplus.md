# Setting up TablePlus

Open TablePlus and right-click to start a  new connection:

Choose PostgreSQL (for PostgreSQL obviously):

The default values should work fine:

Every time I have done this, I have got an error that the database <username>, e.g. pablojoyce, does not exist. 

To fix this, in terminal, enter createdb <username>, e.g. createdb pablojoyce. Then try again to open the new connection.