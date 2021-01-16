## This is [Patientor-Backend](https://github.com/SonTrungTo/Fullstack-2020-Helsinki/tree/master/part9/patientor/backend)...

from the Patientor App in FullStack 2020, running in Docker container.

To execute the program, run:

1. docker build -t patientor-backend .
1. docker container run -p 3001:3001 patientor-backend

The app will be available at http://localhost:3001/. The main two apis are:

- http://localhost:3001/api/patients: Show a list of patients, with corresponding medical records. (POST method to
this address will create a new patient)
- http://localhost:3001/api/patient/<patientID>: Show the specific patient.
- http://localhost:3001/api/diagnoses: Show a lit of symptomps.