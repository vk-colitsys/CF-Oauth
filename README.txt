Introduction
------------------------------------------------
OAuth is a ColdFusion implementation of the OAuth protocol (http://oauth.net),
based on the Core 1.0 specification (http://oauth.net/core/1.0/), published on 4th December 2007.

Based on existing PHP OAuth code from Andy Smith (http://term.ie/oauth/example), including:
 - example OAuth-Server implementation (folder oauth),
 - example OAuth-Client implementation (folder examples), 
 - database generation script for MSSQL, PostgreSQL, Oracle (folder database),
 - cfcUnit (http://cfcunit.org/cfcunit) test case files (folder tests)

Public OAuth discussion group at "http://groups.google.com/group/oauth".

For bug reports and suggestions, please send an e-mail to "klein@contens.de"

Requirements
------------------------------------------------
ColdFusion, Railo 2.0, MSSQL or PostgreSQL or Oracle database

License
------------------------------------------------
OAuth 0.8.2 is released under the Apache 2.0 license.

Copyright 2008 CONTENS Software GmbH

Licensed under the Apache License, Version 2.0 (the "License"); 
you may not use this file except in compliance with the License. 
You may obtain a copy of the License at 

	http://www.apache.org/licenses/LICENSE-2.0 

Unless required by applicable law or agreed to in writing, software 
distributed under the License is distributed on an "AS IS" BASIS, 
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. 
See the License for the specific language governing permissions and 
limitations under the License.

Installation
------------------------------------------------
1.	Create an empty database and ColdFusion DSN called "oauth"

2.	If you are using a MSSQL database, you don't have to modify the variables in the file "database/create_tables.cfm".
	Otherwise you have to modify the variable "sDbsys" for the database platform in use.

3.	Execute "database/create_tables.cfm"

4.	Configure the base URL and endpoint links in the file "examples/common.cfm"

5.	Copy the folder oauth into your web folder or set a mapping called oauth for this folder

6.	Create a consumer in "examples/admin_consumers.cfm" with the values consumer key = CONSUMER_KEY and consumer secret = CONSUMER_SECRET

7.  Now you can browse through the example files (examples/index.cfm) and test the endpoints and token generation