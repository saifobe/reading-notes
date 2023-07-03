#  Permissions

### 1.1. What is a permission?

A permission is a rule that defines which users can access which resources and what they can do with those resources.

### 1.2. What is a role?

A role is a collection of permissions that can be assigned to a user.

### 1.3. Why would we use permissions instead of role based authorization?

Permissions are more flexible than roles. For example, you can assign a permission to a specific user, but you can't assign a role to a specific user.

### 1.4. What is a claim?

A claim is a statement about a user that is made by an identity provider. For example, a claim could be that a user is over 18 years old.

### 1.5. What is an API?

An API is a set of functions that allows applications to access data and interact with external software components.

### 1.6. What is a token?

A token is a piece of data that is used to authenticate a user. For example, a token could be a username and password.

# Postgresql

### What is PostgreSQL?

PostgreSQL is a relational database management system (RDBMS) that is used to store data in tables and rows.

### How does PostgreSQL use roles?

PostgreSQL uses roles to control access to databases and tables. For example, a role could be used to grant read-only access to a database.

### What happens if we don’t supply a password to a role?

If we don't supply a password to a role, PostgreSQL will generate a random password for the role.

### How do we create a role?

We can create a role by using the CREATE ROLE statement.

### What is the difference between a user and a role?

A user is a role that has login privileges. A role is a user that does not have login privileges.

### How do we grant a role to a user?

We can grant a role to a user by using the GRANT statement.


