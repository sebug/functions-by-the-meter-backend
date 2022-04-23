# Functions by the Meter - Backend
The idea of this project is to have some Azure functions that we can call and
measure (measurements being thrown away afterwards).

Following this guide: https://www.shanebart.com/deploy-az-func-with-github-actions/ . You have to create at least the credentials in the azure cloud shell (didn't work out when I did it using the cli).

	az group create -n ByTheMeterGroup -l SwitzerlandNorth
	az ad sp create-for-rbac --name "bythemeterapp" \
	--role contributor \
	--scopes /subscriptions/{subscription-id}/resourceGroups/ByTheMeterGroup \
	--sdk-auth

Now create a Github Repo Secret with the JSON you received.

Go to the Azure portal and create an Azure ARM template for the function to be created.



