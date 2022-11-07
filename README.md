# First example to learn and setup express node js
## Express is a routing and middleware web framework (library) in the backend (node js).

Commands :-
- nmp i express
- nmp i --save-dev nodemon
- package.json 
    - "scripts": {
    "devStart": "nodemon server.js"
    },

- nmp run devstart

- import express library -> express=require('express')
- create express server -> app=express() function
- listen to port 3000
- create route -> app.get(path, (req,res)) reqest method
- app.send info to the user -> res.send('text') || res.sendStatus(500) error || res.status(500).json({message:"Error"})
   || res.json({message:"Error"}) || res.wonload("server.js") 
   - || res.render('index') :-
    - npm i ejs  // view engine
    - set view engine as ejs : app.set("view engine","ejs") 
 - || res.render('index',{text : 'world'}) :-
- index.ejs -> run some code coming from the server using <%= locals.text || 'default text' %>

- create many routes -> router=express.Router() function
- router.get()
- use the new route from main server file -> userRouter=require('./routes/users'); app.use('/users',userRouter)
- url with dynamic parameters -> req.params.id
- routerroute.get()  , routerroute.put() , routerroute.delete()
- middleware functions -> req , res , next()