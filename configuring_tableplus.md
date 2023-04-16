# Setting up TablePlus

Open TablePlus and right-click to start a  new connection:
![Screenshot 2023-04-10 at 12 41 08](https://user-images.githubusercontent.com/19639889/232344318-031eb043-8680-4497-a493-af40b1be9760.png)
Choose PostgreSQL (for PostgreSQL obviously):
![Screenshot 2023-04-10 at 12 42 21](https://user-images.githubusercontent.com/19639889/232344348-48a468a1-f0c6-4f5e-acc8-4b8e5b265225.png)
The default values should work fine:
![Screenshot 2023-04-10 at 12 43 25](https://user-images.githubusercontent.com/19639889/232344406-6b6fecb3-ffef-4381-b8be-b275aaae5138.png)
Every time I have done this, I have got an error that the database <username>, e.g. pablojoyce, does not exist. 
![Screenshot 2023-04-10 at 12 44 24](https://user-images.githubusercontent.com/19639889/232344420-52a19ec8-b302-44b0-a350-b94d7ac100c2.png)
To fix this, in terminal, enter `createdb <username>`, e.g. 
```
createdb pablojoyce
```
Then try again to open the new connection.

