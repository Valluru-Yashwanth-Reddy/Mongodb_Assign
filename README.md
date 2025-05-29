# Mongodb_Assign


C:\Users\Minfy>mongosh "mongodb+srv://cluster0.yoxllv9.mongodb.net/" --apiVersion 1 --username valluruyashwanthreddy
Enter password: ****************
Current Mongosh Log ID: 6837e030991e2acfde6c4bcf
Connecting to:          mongodb+srv://<credentials>@cluster0.yoxllv9.mongodb.net/?appName=mongosh+2.5.1
Using MongoDB:          8.0.9 (API Version 1)
Using Mongosh:          2.5.1

For mongosh info see: https://www.mongodb.com/docs/mongodb-shell/

Atlas atlas-dnt69f-shard-0 [primary] test> show dbs
minfy_training  160.00 KiB
todo            128.00 KiB
admin           344.00 KiB
local            33.41 GiB
Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.insertMany([{name:"Docker Image",status:"pending"},
... {name:"AWS EC2 Instances ",status:"completed"},
... {name:"Python basics",status:"pending"},
... {name:"Jenkins Creare a Free Style Project",status:"completed"},
... {name:"CI/CD Pipeline Iclude tests",status:"pending"},
... {name:"Mongodb ",status:"completed"},
... {name:"Lambda",status:"pending"},
... {name:"SonarQube Code anlysis",status:"completed"},
... {name:"Graffana Metrics monitoring",status:"pending"},
... {name:"Linux",status:"completed"}]);
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6837e1a1991e2acfde6c4bd0'),
    '1': ObjectId('6837e1a1991e2acfde6c4bd1'),
    '2': ObjectId('6837e1a1991e2acfde6c4bd2'),
    '3': ObjectId('6837e1a1991e2acfde6c4bd3'),
    '4': ObjectId('6837e1a1991e2acfde6c4bd4'),
    '5': ObjectId('6837e1a1991e2acfde6c4bd5'),
    '6': ObjectId('6837e1a1991e2acfde6c4bd6'),
    '7': ObjectId('6837e1a1991e2acfde6c4bd7'),
    '8': ObjectId('6837e1a1991e2acfde6c4bd8'),
    '9': ObjectId('6837e1a1991e2acfde6c4bd9')
  }
}
Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.find()
[
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd0'),
    name: 'Docker Image',
    status: 'pending'
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd1'),
    name: 'AWS EC2 Instances ',
    status: 'completed'
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd2'),
    name: 'Python basics',
    status: 'pending'
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd3'),
    name: 'Jenkins Creare a Free Style Project',
    status: 'completed'
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd4'),
    name: 'CI/CD Pipeline Iclude tests',
    status: 'pending'
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd5'),
    name: 'Mongodb ',
    status: 'completed'
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd6'),
    name: 'Lambda',
    status: 'pending'
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd7'),
    name: 'SonarQube Code anlysis',
    status: 'completed'
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd8'),
    name: 'Graffana Metrics monitoring',
    status: 'pending'
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd9'),
    name: 'Linux',
    status: 'completed'
  }
]
Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.updateMany({status:"pending"},{$set:{status:false}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 5,
  modifiedCount: 5,
  upsertedCount: 0
}
Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.updateMany({status:"completed"},{$set:{status:true}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 5,
  modifiedCount: 5,
  upsertedCount: 0
}
Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.find()
[
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd0'),
    name: 'Docker Image',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd1'),
    name: 'AWS EC2 Instances ',
    status: true
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd2'),
    name: 'Python basics',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd3'),
    name: 'Jenkins Creare a Free Style Project',
    status: true
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd4'),
    name: 'CI/CD Pipeline Iclude tests',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd5'),
    name: 'Mongodb ',
    status: true
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd6'),
    name: 'Lambda',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd7'),
    name: 'SonarQube Code anlysis',
    status: true
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd8'),
    name: 'Graffana Metrics monitoring',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd9'),
    name: 'Linux',
    status: true
  }
]
Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.updateMany({},{$set:{status:false}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 10,
  modifiedCount: 5,
  upsertedCount: 0
}
Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.find()
[
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd0'),
    name: 'Docker Image',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd1'),
    name: 'AWS EC2 Instances ',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd2'),
    name: 'Python basics',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd3'),
    name: 'Jenkins Creare a Free Style Project',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd4'),
    name: 'CI/CD Pipeline Iclude tests',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd5'),
    name: 'Mongodb ',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd6'),
    name: 'Lambda',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd7'),
    name: 'SonarQube Code anlysis',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd8'),
    name: 'Graffana Metrics monitoring',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd9'),
    name: 'Linux',
    status: false
  }
]
Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.insertOne({name:'L1 update',status:false})
{
  acknowledged: true,
  insertedId: ObjectId('6837e235991e2acfde6c4bda')
}
Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.find()
[
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd0'),
    name: 'Docker Image',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd1'),
    name: 'AWS EC2 Instances ',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd2'),
    name: 'Python basics',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd3'),
    name: 'Jenkins Creare a Free Style Project',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd4'),
    name: 'CI/CD Pipeline Iclude tests',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd5'),
    name: 'Mongodb ',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd6'),
    name: 'Lambda',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd7'),
    name: 'SonarQube Code anlysis',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd8'),
    name: 'Graffana Metrics monitoring',
    status: false
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd9'),
    name: 'Linux',
    status: false
  },
  {
    _id: ObjectId('6837e235991e2acfde6c4bda'),
    name: 'L1 update',
    status: false
  }
]
Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.updateMany({},{$set:{Updated_at:new Date()}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 11,
  modifiedCount: 11,
  upsertedCount: 0
}
Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.find()
[
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd0'),
    name: 'Docker Image',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd1'),
    name: 'AWS EC2 Instances ',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd2'),
    name: 'Python basics',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd3'),
    name: 'Jenkins Creare a Free Style Project',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd4'),
    name: 'CI/CD Pipeline Iclude tests',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd5'),
    name: 'Mongodb ',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd6'),
    name: 'Lambda',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd7'),
    name: 'SonarQube Code anlysis',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd8'),
    name: 'Graffana Metrics monitoring',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd9'),
    name: 'Linux',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e235991e2acfde6c4bda'),
    name: 'L1 update',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  }
]
Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.updateMany({name:'Linux'},{$set:{DeadLine:new Date("2025-05-29T11:19:24.767Z")}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
  }
  Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.find()
[
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd0'),
    name: 'Docker Image',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd1'),
    name: 'AWS EC2 Instances ',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd2'),
    name: 'Python basics',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd3'),
    name: 'Jenkins Creare a Free Style Project',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd4'),
    name: 'CI/CD Pipeline Iclude tests',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd5'),
    name: 'Mongodb ',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd6'),
    name: 'Lambda',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd7'),
    name: 'SonarQube Code anlysis',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd8'),
    name: 'Graffana Metrics monitoring',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd9'),
    name: 'Linux',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z'),
    DeadLine: ISODate('2025-05-29T11:19:24.767Z')
  },
  {
    _id: ObjectId('6837e235991e2acfde6c4bda'),
    name: 'L1 update',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  }
]
Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.updateOne({name:'Graffana Metrics monitoring'},{$set:{DeadLine:new Date()}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.find()
[
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd0'),
    name: 'Docker Image',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd1'),
    name: 'AWS EC2 Instances ',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd2'),
    name: 'Python basics',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd3'),
    name: 'Jenkins Creare a Free Style Project',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd4'),
    name: 'CI/CD Pipeline Iclude tests',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd5'),
    name: 'Mongodb ',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd6'),
    name: 'Lambda',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd7'),
    name: 'SonarQube Code anlysis',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd8'),
    name: 'Graffana Metrics monitoring',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z'),
    DeadLine: ISODate('2025-05-29T04:31:12.420Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd9'),
    name: 'Linux',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z'),
    DeadLine: ISODate('2025-05-29T11:19:24.767Z')
  },
  {
    _id: ObjectId('6837e235991e2acfde6c4bda'),
    name: 'L1 update',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  }
]
Atlas atlas-dnt69f-shard-0 [primary] test>  db.todo.updateOne({_id:ObjectId('6837e235991e2acfde6c4bda')},{$set:{status:true}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.find()
[
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd0'),
    name: 'Docker Image',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd1'),
    name: 'AWS EC2 Instances ',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd2'),
    name: 'Python basics',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd3'),
    name: 'Jenkins Creare a Free Style Project',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd4'),
    name: 'CI/CD Pipeline Iclude tests',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd5'),
    name: 'Mongodb ',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd6'),
    name: 'Lambda',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd7'),
    name: 'SonarQube Code anlysis',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd8'),
    name: 'Graffana Metrics monitoring',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z'),
    DeadLine: ISODate('2025-05-29T04:31:12.420Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd9'),
    name: 'Linux',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z'),
    DeadLine: ISODate('2025-05-29T11:19:24.767Z')
  },
  {
    _id: ObjectId('6837e235991e2acfde6c4bda'),
    name: 'L1 update',
    status: true,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  }
]
Atlas atlas-dnt69f-shard-0 [primary] test> db.todo.find({Updated_at:{$gt: new Date(new Date().getTime()-10*60*1000)}})
[
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd0'),
    name: 'Docker Image',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd1'),
    name: 'AWS EC2 Instances ',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd2'),
    name: 'Python basics',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd3'),
    name: 'Jenkins Creare a Free Style Project',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd4'),
    name: 'CI/CD Pipeline Iclude tests',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd5'),
    name: 'Mongodb ',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd6'),
    name: 'Lambda',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd7'),
    name: 'SonarQube Code anlysis',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd8'),
    name: 'Graffana Metrics monitoring',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z'),
    DeadLine: ISODate('2025-05-29T04:31:12.420Z')
  },
  {
    _id: ObjectId('6837e1a1991e2acfde6c4bd9'),
    name: 'Linux',
    status: false,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z'),
    DeadLine: ISODate('2025-05-29T11:19:24.767Z')
  },
  {
    _id: ObjectId('6837e235991e2acfde6c4bda'),
    name: 'L1 update',
    status: true,
    Updated_at: ISODate('2025-05-29T04:29:37.079Z')
  }
]
Atlas atlas-dnt69f-shard-0 [primary] test>
