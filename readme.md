This powershell cmdlet installs the sqlps powershell extensions in your powershell v2 shell. 

This means you can run invoke-sqlcmd and do all the other goodness from your regular powershell cmdlets. 

This requires having Sql Server Powershell installed. (e.g. Sql 2008 r2 management tools) 

Installation 
============

Put the PsSql.psm1 file in a modules folder -  $Env:PSModulePath

OR

(Soon - once it's approved) If you have <a href="https://github.com/psget/psget">PsGet</a> installed, you can execute:

    install-module PsSql

Usage
=====

Load the module with: 

	Import-Module PsSql

Then use the cmdlets etc as you wish. e.g.
	
	Invoke-sqlcmd -serverinstance server -database AdventureWorks -query "select * from somewhere"

	