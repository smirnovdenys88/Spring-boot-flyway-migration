Here, spring.jpa.hibernate.ddl-auto can be none, update, create, or create-drop. See the Hibernate documentation for details.

if create from Entity
none: The default for Posgtres. No change is made to the database structure.
update: Hibernate changes the database according to the given entity structures.
create: Creates the database every time but does not drop it on close.
create-drop: Creates the database and drops it when SessionFactory closes.

if use Flyway
spring.jpa.hibernate.ddl-auto=validate
validate: Validates current database schema against available migrations

Migration flyway
<dependency>
    <groupId>org.flywaydb</groupId>
    <artifactId>flyway-core</artifactId>
</dependency>