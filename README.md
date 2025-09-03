## Usage

Before usage need to create network for correct dependencies work:

```shell
task -d scripts network -v
```

To run all microservices and theirs dependencies in
docker, use next command (twice due to migrations work logics):

```bash
task -d scripts up -v
```

To stop all microservices and theirs dependencies,
use next command:

```bash
task -d scripts down -v
```

To clean up all created dirs and docker files, use next command:

```bash
task -d scripts clean_up -v
```

## Database

To connect to database container, use next command:

```shell
task -d scripts connect_to_database
```

To connect to DB inside database container, use next command:

```shell
psql -U $POSTGRES_USER
```

To create backup of database, use next command:

```shell
task -d scripts backup
```

To restore database from latest backup, use next command:

```shell
task -d scripts restore
```

To restore database from specific backup, use next command:

```shell
task -d scripts restore BACKUP_FILENAME={{backup_filename}}
```
