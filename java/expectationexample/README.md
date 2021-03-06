Expectation Sample
========================

This sample application demonstrates how to write a stored procedure using expectations for query result validation rather than writing extra branching logic.

VoltDB Requirements
===================
Sample requires VoltDB 2.8.3 or higher.

Running The Sample
==================
The application requires very little to run.

Setup
=====
Running the application requires either two or three consoles depending on how
deep you want to go.

The two console version builds and runs both the server and the client. The
three console version opens sqlcmd so that you can perform additional queries
and explore some of the analytical aspects of VoltDB using just ad hoc queries.

Execute the following in all terminals.
Export VOLT_HOME=<you voltdb home directory>

Building and Running
====================
Execute the following to build the stored procedures and the client application.
You must perform the "clean" step whenever you change the stored procedure or
the client.

Do the following in the first terminal:

    ./run.sh clean
    ./run.sh server

Step one will delete all the compiled code and jar file.
Step two will compile everything and start the volt server.

In the second terminal, run the following:

    ./run.sh client

This will begin the client application. The client application is configured to
connect to one VoltDB instance running on the local host. The application will then display the results of one good login attempt and two bad login attempts for both a traditional, or simple, logic test vs the expectation method.
