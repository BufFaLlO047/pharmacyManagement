Pharmacy Management System

--------------------------------------------------------------------------------------------------------------------------------------------------------------

INSTALLATION AND PROJECT INITIALISATION:

Refer: https://blog.logrocket.com/build-rest-api-typescript-using-native-modules/

npm init -y


npm install -g typescript
npm install -D ts-node
npm install @types/node

refer in:
src/index

GET by ID : needs to be updated. 

#POST : Latest ID checks for only maximum ID possible. DELETED ID replacement is required.
--------------------------------------------------------------------------------------------------------------------------------------------------------------
The below assigns task.id to the missing ID obtained from tasks[index].id. 
The below line checks for missing ID in ascending order with reference to index array having latest_ids as continous numberical array and assigns it to task.id.
If task.id is NULL or 0 ( no missing IDs in DB), then task.id is updated with latest_id+1 and assigned directly to the post message.
task.id = index.filter(x => !tasks.find(f=>f.id == x))
if(task.id == null || task.id == 0)
{
    task.id = latest_id+1
}

--------------------------------------------------------------------------------------------------------------------------------------------------------------

DELETE: Request ID parameter is in body. Needs to be in header

#POST: Manufacture date should not be newer than today's date. Expiry date cannot be older than today's date. CODED

#PATCH/PUT: If quantity is 0, then change medicine name paramter to "Medicine Name - Not Available".

To find an algorithm to enable 2 or more medicines POST call with different manufacture and expiry date as different sets of medicines. 


