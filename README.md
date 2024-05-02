# Pretender

This library lets you pretend you have a horizontally scalable 'wide column'
database, and yet use a relational database like PostGreSQL because you
don't currently have the volume of data to justify using AWS DynamoDB.

# FAQ

## Why bother?

By modeling your data 'as if' it was using a wide-column store, if you
ever need to migrate to DynamoDB, it will be super easy. This model is
performant on relational data too, so you are not sacrificing anything
by starting this way. Just giving you an easy out if you need to scale.

You know, cause you totally will have to one day, right?

## Is this compatible with DynamoDB?

That would be great. Ideally this has a driver similar to DynamoDB's AWS
driver, so you just need to change packages to use the real thing. We 
should totally do that. 

## How easy is it to export my data from here to DynamoDB?

The end goal is to have a command that allows for table creation in DynamoDB,
and a chunk-exporter for data to go into DynamoDB. 

## Do you really want to write a weird ORM?

Uh....