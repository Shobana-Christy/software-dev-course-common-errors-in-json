                                         // removed declaring variable name -- they are meant for data storage not executable code
{
  "hotelName": "Grand City Hotel",
  "checkInDate": "2024-05-15",            // fixed commas
  "checkOutDate": "2024-05-20",
  "guests": [
    {
      "name": "Alice Johnson",           //fixed double quotes 
      "age": 30,
      "email": "alice.johnson@example.com"
    },
    {
      "name": "Bob Smith",
      "age": null,                          // unsupported type with valid json types.
                                             // So used null instead of undefined
      "email": "bob.smith@example"
    }
  ],
  "roomDetails": {
    "type": "Suite",
    "pricePerNight": 200,
    "amenities": ["WiFi", "Breakfast", "Parking"]  //removed comma after the element
  }
}





Error 1 - Variable Declaration
     • What was wrong?
       JSON is declared in variable const.

     • Why is it a problem in JSON?
       JSON files are meant to be for data storage, not for executable code.

     • What did you change to fix it?
       I removed const invalidBookingJSON and template literals on that line.



   Error 2 - Missing Comma in key-value pair
     • What was wrong?  
         A comma was missing in between key-value pairs inside  the objects.

     • Why is it a problem in JSON?
        JSON requires comma to seperate each key-value pairs in an object. Without comma, 
        the parse doesn't know to parse where the pair - starts ends and 
        the next  begins which cause syntax error.
          
     • What did you change to fix it?
        I added missing comma between the key-value pairs.


    Error 3 - Missing double quotes in the string  
     • What was wrong?  
         The key in the object was missing double quotes.

     • Why is it a problem in JSON?
        In JSON, all object's key should be enclosed in double quotes. Without them, 
        the file won't parse correctly.

     • What did you change to fix it?
        I added double quotes in the object's key.


    Error 4 - value is assigned as undefined.
     • What was wrong?
         The value in the age is undefined.

     • Why is it a problem in JSON?
         Only specific data types are supported by JSON. JSON doesn't supports 'undefined' 
         data type which makes invalid JSON.

     • What did you change to fix it?
         I fixed it by changing undefined to null.
         
    Error 5 - Trailing comma in array
     • What was wrong? 
       There is trailing comma after the array element.

     • Why is it a problem in JSON?
        In JSON trailing comma after the last item is invalid.

     • What did you change to fix it?
        I removed the trailing comma after the last element in the array.
*/


// ============================================
// 🤔 Follow-Up Questions
// ============================================

/*
💬 Reflect and answer the following:

1️⃣ What tools or techniques did you use to identify the errors?
    
       I created JSON file and pasted the code into to detect syntax errors. The editor 
    highlighted issues such as missing quotes and commas, which I corrected. 
    Additionally I used  https://jsonlint.com/ to validate the structure and 
    identify remaining errors.

2️⃣ How did you confirm that your corrected JSON file was valid?
       When the errors were fixed the JSON validator displayed that the JSON file was valid.

3️⃣ Which errors were the most difficult to spot? Why?
        Strings without double quotes in keys, missing commas in objects, extra trailing 
        comma were difficult to spot.These were tricky because  they are having 
        more string values and nested structures with comma seperated for objects and arrays. 

4️⃣ What strategies can help you avoid these kinds of errors in the future?
   (e.g., syntax highlighting, linters, writing JSON by example)
        Using syntax highlighting, linters and editors can help prevent errors.
        Also understanding where the error occurs and writing JSON example 
        can make the process easier and help to avoid  errors in the future.
       

*/
