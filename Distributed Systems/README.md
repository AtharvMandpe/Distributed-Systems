Distributed Systems Project

Overview:
This project implements a remote, asynchronous dictionary lookup service using Servlet/JSP and Java RMI frameworks.

Functionality:

A JSP page allows users to input a string for dictionary lookup.
The request is dispatched to a servlet, queued in an inQueue, and assigned a job ID, which is returned to the client.
The client polls the server periodically for the result.
A remote DictionaryService processes requests via RMI, returning the definition or "String not found." The result is added to an outQueue and sent to the client.
Key Features:

Remote Lookup: DictionaryService interface with lookup(String s) method for dictionary queries.
Asynchronous Processing: Requests are queued, processed periodically, and handled concurrently with multithreading.
REST API Integration: Communicates with the JSP page through a RESTful service using Jersey.
Enhanced Dictionary: Uses a ~94,000-word dictionary based on Webster’s Dictionary.
SPA Design: Web application designed as a single-page application for faster response times.
CRUD Functionality: Supports adding, modifying, and removing words in the in-memory dictionary (case-insensitive).
Execution Steps:

Dictionary Service: Create a JAR file and start the RMI service.
Web Application: Deploy the WAR file on Tomcat and access the application via http://localhost:8080/job-server/.
Conclusion:
This project demonstrates distributed systems communication using Java RMI for homogeneous systems and REST APIs for heterogeneous systems, showcasing the integration of multiple communication models.
