# snowflake-datawarehouse

The [Snowflake](https://www.snowflake.com/) data warehouse is a cloud based software as a service data warehouse platform built for big data a wide scale data computation.

## Architecture

The architecture of Snowflake consists of the following components:

- databases
- data shares
- data warehouses
- services

## SnowSQL CLI

Download the SnowSQL CLI installer from [here](https://sfc-repo.snowflakecomputing.com/snowsql/bootstrap/index.html).

### Test Connection

    snowsql -a bu64242.central-us.azure -u MICHAELSLOWER

## Add connection information to config file

Find config file at `~/.snowsql/config`

    [connections.sf]
    #Can be used in SnowSql as #connect example

    accountname = bu64242.central-us.azure
    username = MICHAELSLOWER
    password = <pw>
    dbname = data_db
    warehousename = compute_wh
    schemaname = public

    [options]
    auto_completion = True

    prompt_format=>>

Once the config file has at least one `[connections.<name>]` defined, you can connect to Snowflake using the following command:

    snowsql -c <name>

## Bulk Loading Data

- Move file(s) into a Staging area.
  - Each Table and User has a Stage.
  - Can also create named Stage.
- 
