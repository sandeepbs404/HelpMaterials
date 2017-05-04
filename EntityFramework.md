# What is EF?
#Why use EF?
Does it fits our needs?


Creating Connection and commands, and  it's execution is taken care by EF.
Create and execute queries.
Prcoess Results
Materialise objects from results

Uses:
More Flexablity  between the definitions of your domain classes and schema of ur database. So that we create domain classes that makes more sense for you domain, database schema to be designed in most effective within database.
Can be done by Mappings.

Uses:
Developer Productivity- Easy to learn
-LINQ common for object and entities.
-No direct interact to Database, that worrying about database, concentrate and deal in terms of domain classes.


How it works:
Domain Classes(Your Code) ->EF-DBContext to wrap Domain classes into Model ->DataBase
1. Domain Classes- Simple C# classes
2. EF API(DBCOntext)
	1. Map Domain Classes to DB Schema
	2. Transalate & execute Queries
	3. Track Changes : keeps track of object as long as they are in scope
	4. Infer and Execute Updates(SaveChanges()).
	
	
Models:
1. Visual Model  (VS by designer - EDMX to classes is automatically done): EDMX->In-Memory Rub-Time Metadata
2. Straight code(C#) Code first : Class->In-Memory Rub-Time Metadata

From both the approaches it creates In-Memory Rub-Time Metadata

POCO - Plain Old CLR Objects

2008(EF1) ->2010(EF4)

DBContext
1. Map Domain Classes to DB Schema
	2. Transalate & execute Queries
	3. Track Changes : keeps track of object as long as they are in scope
	4. Infer and Execute Updates(SaveChanges()).
IDbSet
	1. Is the organisational unit that maintains a particular set of types.
	2. Is resposible for maintaining the in-memory collection of entities in your model.
	3. You perform your queries through DBSets, asking DBContext to query by way of the DBSet->Finally EF interprets into query
	
	
EntityFramework.Utilities
