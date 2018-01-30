# mongoDb

// Get all docs

        db.restaurants.find();

// Limit/sort

      db.restaurants.
        find().
        sort({name: 1}).
        limit(10);

// Get using _id

      var myId = db.restaurants.findOne({}, {_id: true})._id;
      db.restaurants.findOne({_id: myId});

// Get by descriptor

      db.restaurants.find({borough: "Queens"});

// Count all docs

      db.restaurants.count();

// Count using a nested value

    db.restaurants.find({'address.zipcode': '11206'}).count()

// delete by id

    var myId = db.restaurants.findOne({}, {_id: true})._id;
    db.restaurants.removeOne({_id: myId});

// update one doc

    var myId = db.restaurants.findOne({}, {_id: true})._id;
    db.restaurants.updateOne(
      {_id: myId},
      {$set: {name: 'yummy yum yum's'}});

// update many documents

    db.restaurants.updateMany

