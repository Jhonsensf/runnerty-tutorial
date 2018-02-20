# Runnerty Tutorial

This a [Runnerty](https://github.com/runnerty/runnerty) tutorial divided in several steps.

It's a step by step workflow which is going to load a file with several records into a database, generate an inform and send an email to all the users of the database.


## First step

In this step the chain loads the file ./new_users.csv into the Mysql Database.

> This example uses the @runnerty_mysql_executor, to follow this tutorial you should have a Mysql Database


### Testing

Clone the repo
```
https://github.com/Jhonsensf/runnerty-tutorial
```

Go to the directory  
```
cd runnerty-tutorial
npm install
```

Open the project in the editor and change you Database cofiguration in the ./config.json file:

```
{
	"id": "mysql_default",
	"type": "@runnerty-executor-mysql",
	"host": "localhost",
	"user": "root",
	"password": "root",
	"database": "MYSCHEMA",
	"port": "3306"
}
```
Executes the ./table.sql in you Database to crete the test schema and the users table.

Run the Chain
```
run -f MY_CHAIN
```

> The chain will load the users, in the next step we are going to configure the chain to get noticed when it ends using notifiers