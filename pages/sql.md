---
title: SQL Quickstart
id: sql
---

# SQL Quickstart

When you first open the dashboard, you’ll be greeted by a “Welcome to Pacuare Reserve!” screen (if you have full access, this screen will be skipped; this screen shows while restricted accounts’ personal databases are being created), followed by the main screen. In the center should be two tabs, SQL (the initial one) and Python. Stick to SQL for now.

Inside the SQL view, there'll be a query editor on the left and a results view on the right. Queries in the query editor will be run either on your personal copy of the database or, if you have full access, on the main database itself. If you have full access, **be careful!**

> **Tip:** The [Neon PostgreSQL tutorial](https://neon.tech/postgresql/tutorial) is a great way to get started with PostgreSQL, which is what the Pacuare database uses.

> **Note:** If you try to run multiple statements at once, you’ll get an error! This is because the app runs your query as one single prepared statement, which can (as the name suggests) only contain one statement. For more complicated queries, consider making a stored function.

## Augh! My database is broken!
If you have a full-access account, this is a problem. Please contact an administrator.

If you have a limited-access account, though, putting your data back in order is easy. Open your account settings with the gear icon in the upper-right corner.

If the data in your `pacuare_raw` table is corrupted, and you’d like to keep everything else, click **Refresh Data**. This will delete all of the rows in the table and re-import from the master database. If the structure is corrupted, or if something else in the database is broken, click **Recreate Database**. This will effectively delete and recreate your account and all of your data, so use it judiciously.
