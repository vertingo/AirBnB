## 📝 Author
[<img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/854371/profile/profile-80_2.jpg" align="right">](http://ddcreationstudios.at/)
Download MongoDB:
https://www.mongodb.com/fr

Install MangoDB!
Installation command:

C:\DevelopeWithVertin\MEAN\env\mongodb\bin\mongod.exe --dbpath C:\DevelopeWithVertin\MEAN\env\data

Launch MongoDb:
C:\DevelopeWithVertin\MEAN\env\mongodb\bin\mongo.exe

In the command prompt of Visual Studio Code type:
npm install mongoose

Add this to your models user.js for exemple
var mongoose = require('mongoose');

Establish a connection to your mongo database:
mongoose.connect('mongodb://localhost/testForAuth', function(err) {
  if (err) { throw err; }
});

Create a table in your user.js remember that you don't need to type sql query with MongoDB
var commentaireArticleSchema = new mongoose.Schema({
  pseudo : { type : String, match: /^[a-zA-Z0-9-_]+$/ },
  contenu : String,
  date : { type : Date, default : Date.now }
});

Insert data in your database:
// On le sauvegarde dans MongoDB !
monCommentaire.save(function (err) {
  if (err) { throw err; }
  console.log('Commentaire ajouté avec succès !');
  // On se déconnecte de MongoDB maintenant
  mongoose.connection.close();
});


Open a commande prompt and launch the binary file an type the following command to verify that your data has been added properly!
 use blog
switched to db blog
 show collections
commentaires
system.indexes
 db.commentaires.find()
{ « contenu » : « Salut, super article sur Mongoose ! », « pseudo » : « Atinux », « _id » : ObjectId(« 4e995dab2ea479d40f000001?), « date » : ISODate(« 2011-10-15T10:17:15.829Z ») }


# 🌐 Authentication Example with Node.JS and MongoDB ![App Progress Status](https://img.shields.io/badge/Status-Finished-0520b7.svg?style=plastic)

---
A simple example to show how authentication is implemented with Node.JS and MongoDB.
---

<img src="./preview.png" alt="pic"/>


Check out my [post on medium.com](https://medium.com/@ddcreationstudi)

You can find a more detailed tutorial at treehouse:
<a href="http://referrals.trhou.se/danieldeutsch3" target="_blank"><img src="https://static.teamtreehouse.com/assets/content/referral-badge-grn.png" height="150"/></a>

```
A little boost follow us on YouTube and Facebook!
[You Tube]: https://www.youtube.com/channel/UC2g_-ipVjit6ZlACPWG4JvA?sub_confirmation=1
[Facebook]: https://www.facebook.com/vertingo/
```

<p align="center">
  <a href="https://www.youtube.com/channel/UC2g_-ipVjit6ZlACPWG4JvA?sub_confirmation=1"><img src="https://platform-media.herokuapp.com/assets/images/reseaux-sociaux/youtube2.png" width="400" height="250"/></a>
  <a href="https://www.facebook.com/vertingo/"><img src="https://platform-media.herokuapp.com/assets/images/reseaux-sociaux/rejoins_nous.png" width="400" height="250"/></a>
</p>
