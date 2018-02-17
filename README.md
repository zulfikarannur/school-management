# School Management v 1.0.0

This is backend application for simple school management.

This is still on-build.

## Feature
For this version the current feature is:

1. Different user with different roles (explanation below)
2. See sylabus for each teacher and link it with test and homework
3. Admin can add / modify / update / delete other roles
4. Teacher can give homework and test
5. Student can see homework and test
6. Each teacher have their classes, a teacher can have many class
7. Soft delete

Next Release: 
1. Teacher can input homework and score test.
2. Student can see their current report.
3. Teacher can make absent report of their student.
4. Teacher can make a exercise for their student, beside test and homework.

For roles:

| Roles | Capability |
|:---| :----|
| Admin   | Manage other user. See teacher syllabus, homework and test |
| Student | Can see homework and test |
| Teacher | Can modify homework and test |

## REST Resource

| Method | Route | Resource |
|:---: |:---|:---|
| POST| /user | Created user attribute |
| GET | /user | All created users attr|
| GET | /user/:user_id | User with requested id |
| DELETE | /user/:user_id | Soft deleted user |
| PATCH | /user/:user_id | Updated user |
| POST | /syllabus | Created sylabus |
| GET | /syllabus | Get all syllabus created |
| GET | /syllabus/:syllabus_id | Get requested syllabus |
| PATCH | /syllabus/:syllabus_id | Updated syllabus |
| DELETE | /syllabus/:syllabus_id | Soft deleted syllabus |
| POST | /class | Class created |
| GET | /class | All created classes|
| PATCH | /class/:class_id | Updated class |
| DELETE | /class/:class_id | Soft deleted class |
| POST | /class/:class_id/homework | Created homework for class |
| POST | /class/:id/test | Created test for class |
| PATCH | /class/:class_id/homework/:homework_id | Updated homework |
| PATCH | /class/:class_id/test/:test_id | Updated test |
| DELETE | /class/:class_id/homework/:homework_id | Deleted homework |
| DELETE | /class/:class_id/test/:test_id | Deleted test |
| GET | /class/:class_id/ | All homework and test in a class |
| GET | /class/:class_id/homework/:homework_id | Requested homework |
| GET | /class/:class_id/test/:test_id | Requested test | 
