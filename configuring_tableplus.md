# Setting up TablePlus

I have never been able to have this working right out of the box as Maker's instructions suggest. So do yourself a favour and follow these instructions.

* Look at the terminal output when you install PostgreSQL. It will liklely prompt you to run some commands.
* When last installing PostgreSQL@15, I needed to run the first of these commands and was advised to run the following two:
```
echo 'export PATH="/usr/local/opt/postgresql@15/bin:$PATH"' >> ~/.zshrc
export LDFLAGS="-L/usr/local/opt/postgresql@15/lib"
export CPPFLAGS="-I/usr/local/opt/postgresql@15/include"
```
* Then run `createdb <username>` to create a database for your user. E.g. `createdb pablo`.
  
After that, everything should work fine.

Open TablePlus and right-click to start a  new connection:

![Screenshot 2023-04-10 at 12 41 08](https://user-images.githubusercontent.com/19639889/232344318-031eb043-8680-4497-a493-af40b1be9760.png)

Choose PostgreSQL (for PostgreSQL obviously):

![Screenshot 2023-04-10 at 12 42 21](https://user-images.githubusercontent.com/19639889/232344348-48a468a1-f0c6-4f5e-acc8-4b8e5b265225.png)

The default values should work fine:

![Screenshot 2023-04-10 at 12 43 25](https://user-images.githubusercontent.com/19639889/232344406-6b6fecb3-ffef-4381-b8be-b275aaae5138.png)

Every time I have done this (as explained at the top of this page), I have got an error that the database <username>, e.g. pablo, does not exist. 

![Screenshot 2023-04-10 at 12 44 24](https://user-images.githubusercontent.com/19639889/232344420-52a19ec8-b302-44b0-a350-b94d7ac100c2.png)

To fix this, in terminal, enter `createdb <username>`, e.g. 
```
createdb pablo
```
Then try again to open the new connection.

