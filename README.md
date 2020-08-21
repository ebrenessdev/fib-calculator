# fib-calculator

This is the base project without any Docker configuration

## client
React app which sends requests to the express back-end

## server
express back-end which connects to redis and postgres.
On Redis the history of calculations is stored
On Postgres there is a table 'values' with the list of all fibonacci indexes requested

## worker
a javascript app which is listening for new data on redis
this data is the fibonacci index that a user requests. 
