# How to build NodeJS Express REST API to Upload Image using Multer(PostgreSQL)
this is a simple crud working with images just to test Postgres with Multer . NodeJS and Express

# NB do not forget to insert the database schema file to make way for file storage
this is an API endpoint to insert the single file
http://localhost:5050/upload/upload-single-image
<img  src=https://github.com/TommyTeaVee/imageUpload/blob/fee2f0a97c781b2d160121e5439bfd0c3393cb7f/imageUpload/images/Screenshot%202022-04-27%20at%2002.29.54.png>

- this is an endpoint for inserting multiple files
http://localhost:5050/upload/upload-multiple-image
![alt text] https://github.com/TommyTeaVee/imageUpload/blob/fee2f0a97c781b2d160121e5439bfd0c3393cb7f/imageUpload/images/Screenshot%202022-04-27%20at%2002.38.38.png

# PGAdmin
https://github.com/TommyTeaVee/imageUpload/blob/fee2f0a97c781b2d160121e5439bfd0c3393cb7f/imageUpload/images/Screenshot%202022-04-27%20at%2002.44.36.png

# Experimental not tested
- There is an incomplete POC in the folder frontend. the HTML Script needs to be fixed to post data properly using database schema filters
- The angular folder needs to be changed and properly routed to the correct API
here are the screenshots in order
Writing the input field of type file in the angular reactive form. After click the submit button, it will run the submitPhoto function.
Angular reactive form
https://github.com/TommyTeaVee/imageUpload/blob/master/imageUpload/frontend/angular/1_6ygf1E5B_It-zkVui3wi7Q.png

In the ‘fileChoosen’ function it will create file type and store it in ‘this.image’ variable. In ‘submitPhoto’ function it create a formdata array and append ‘this.image’ with tag ‘profileImage’. We will send this formdata array to the the backend server API using a post request.

Angular Typescript
https://github.com/TommyTeaVee/imageUpload/blob/master/imageUpload/frontend/angular/1_mtjtXx2SwFXLJE33KVbyYg.png

This completes the frontend part of the code to send the file to backend. Now let’s look at how to write the Api using ‘Multer’ in NodeJs to store the File in the server.
https://github.com/TommyTeaVee/imageUpload/blob/master/imageUpload/frontend/angular/1_-Y71msd3XVp6Q4c9BnhWQw.png

