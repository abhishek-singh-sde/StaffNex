# StaffNex

We can simply use Postman to utilize the desired method, and invoke the endpoint accordingly.
The following examples just contain sample invocations with expected body and response.
 
Creating a new employee:
POST 
https://szfgvcv9f0.execute-api.us-east-1.amazonaws.com/production/employee
Body-
{
    "employeeid":"101",
    "job_title":"CEO",
    "full_name":"John Fernandes",
    "Salary":125000
}

Fetching a particular employee:
GET 
https://szfgvcv9f0.execute-api.us-east-1.amazonaws.com/production/employee?employeeid=103

Sample output-
{
    "job_title": "SDE",
    "Salary": 50000,
    "employeeid": "103",
    "full_name": "Jennifer Rose"
}





Fetching list of all employees:
GET 
https://szfgvcv9f0.execute-api.us-east-1.amazonaws.com/production/employees
<Sample Output>{
    "employees": [
        {
            "job_title": "SDE",
            "Salary": 50000,
            "employeeid": "103",
            "full_name": "Jennifer Rose"
        },
        {
            "job_title": "CTO",
            "Salary": 100000,
            "employeeid": "102",
            "full_name": "Adam Linus"
        },
        {
            "job_title": "SDE",
            "Salary": 50000,
            "employeeid": "104",
            "full_name": "Yin Wang"
        },
        {
            "job_title": "CEO",
            "Salary": 125000,
            "employeeid": "101",
            "full_name": "John Fernandes"
        }
    ]
}
Updating a particular employee:
PATCH
https://szfgvcv9f0.execute-api.us-east-1.amazonaws.com/production/employee

Body-
{
    "employeeId":"102",
    "updateKey":"Salary",
    "updateValue":"90000"
}

Deleting a particular employee:
DELETE
https://szfgvcv9f0.execute-api.us-east-1.amazonaws.com/production/employee

Body-
{
    "employeeId":"104"
}
