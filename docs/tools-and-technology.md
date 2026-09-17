# Tools and Technology

**Express** is a Node.js library for building a server with clear routes such as `GET /options` and `PUT /options/:id/vote`. We choose it because the project needs several request paths and Express makes those paths readable; writing the same routing work directly with Node's raw `http` tools would require more manual handling.

**MySQL** is the database program that stores Poll Maker options and votes in a table. We choose it because data must remain after a browser refresh and server restart; without it, option data would only live temporarily in JavaScript memory.

**mysql2** is the Node.js package that lets Express send raw SQL to MySQL and receive rows back. We choose it so students can write and understand real `SELECT`, `INSERT`, `UPDATE`, and `DELETE` queries instead of using an ORM that hides SQL.

**Git** records the history of the project as small commits, while GitHub hosts that history and pull requests online. We choose them so each task has a recoverable checkpoint and a teammate can review it; without Git, file copies and manual sharing would not preserve a clear change history.