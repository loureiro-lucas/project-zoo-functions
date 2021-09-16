# Zoo Functions Project 🚀

The Zoo Functions Project was developed focusing in improve our __ES6 JavaScript__ skills, such as __Higher Order Functions__ (__forEach__, __find__, __some__, __every__, __sort__, __map__, __filter__ and __reduce__) and __Spread Operator__, __Rest Parameters__, __Destructuring__ and much more.

Furthermore, __soft skills__ like _time management__ were essencial for the sucess of the project.

---

`Requirements:`

- #### 1 - Implement the function `getSpeciesByIds`

This function is responsible for searching the animal species by id. It returns an array containing the species referring to the ids passed as a parameter, which can receive one or more ids.

  - If it receives no parameters, it must return an empty array.

- #### 2 - Implement the function `getAnimalsOlderThan`

This function, from the name of a species and a minimum age, checks if all animals of that species have the specified minimum age and returns a boolean.

- #### 3 - Implement the function `getEmployeeByName`

This function is responsible for searching for employee through their first or last name.

  - Without parameters, returns an empty object;
  - When the employee's first or last name is provided, the employee's object must be returned.

- #### 4 - Implement the function `getRelatedEmployees`

Divide it into two functions:
  
`isManager` - who will be responsible for verifying whether a employee is a manager or not.

`getRelatedEmployees` - which uses the first function to display the following outputs:
  - if it is a manager, it must return an array containing the names of the employees it is responsible for;
  - if it is not a manager, an error generated with the constructor function **Error** of the standard JavaScript library should be thrown with the message "The id entered is not of a manager!".
<br>

- #### 5 - Implement the function `countAnimals`

This function is responsible for counting the number of animals of each species.

  - If no arguments are passed, it returns an object whose name of each species is a key to that object, and the total number of animals of that species is its value;
  - With the argument `{ specie: 'penguins' }`, returns a number, the number of penguins in the zoo;
  - With the argument `{ specie: 'giraffes', gender: 'female' }`, it returns a number, the number of female giraffes.
<br>

- #### 6 - Implement the function `calculateEntry`

This function will receive an array of visitors in the following format:

```javascript
const entrants = [
  { name: 'Lara Carvalho', age: 5 },
  { name: 'Frederico Moreira', age: 5 },
  { name: 'Pedro Henrique Carvalho', age: 5 },
  { name: 'Maria Costa', age: 18 },
  { name: 'Núbia Souza', age: 18 },
  { name: 'Carlos Nogueira', age: 50 },
];
```

You must isolate the part of the logic in the `countEntrants` function that is in the same file as the `calculateEntry` function. It should receive the array of visitors and return an object with the count according to the following classification criteria:

* People under the age of 18 are classified as children (child);
* People aged 18 years or over and under 50 are classified as adults (adult);
* People aged 50 years and over are classified as older people (senior).

The function's return must be an object in the following format: `{ child: 3, adult: 2, senior: 1 }`.

- #### 7. Implement the function `getAnimalMap`

The function is responsible for the geographic mapping of species and their animals, and can also filter them by alphabetical order and gender.

- Without parameters, returns animals categorized by location;
- With `includeNames: true` option specified, returns animal names;
- With `sorted: true` option specified, returns sorted animal names;
- With `sex: 'female'` or `sex: 'male'` option specified, returns only male/female animal names;
- With the `sex: 'female'` or `sex: 'male'` option specified and the `sort: true` option specified, it returns only male/female animal names with the animal names sorted;
- Only returns ordered and gendered information if `includeNames: true` is specified, else returns aninals categorized by location.

- #### 8. Implement the function `getSchedule`

The function is responsible for making the animals' time information available in a query to the user, who may want to have access to the schedule of the week, of a day or of a specific animal.

- Without parameters, returns the times for each day and which animals will be available;
- With parameters that are neither an animal nor a day, it returns the times for each day and which animals will be available;
- If a single day is passed, it returns the times for that day and which animals will be available;
- If an animal's name is passed, it must return an array with the days it will be displayed.

- #### 9. Implement the function `getOldestFromFirstSpecies`

The function searches for information on the oldest animal of the first species managed by the employee in the parameter.

- #### 10. Implement the function `getEmployeesCoverage`

This function will be responsible for associating employee coverage information.

The coverage must be represented by an object with the following properties:

```javascript
{
  "id": "4b40a139-d4dc-4f09-822d-ec25e819a5ad", // person id
  "fullName": "Sharonda Spry", // fullname: firstName + lastName
  "species": [ "otters", "frogs" ], // species for which the person is responsible
  "locations": [ "SE", "SW" ], // an array containing all species locations
}
```

The function must receive an options object that will determine its behavior, as follows:

* **name**: The first or last name of the person to be searched
* **id**: The id of the person to be searched

- When called without arguments, it should return an array with the coverage of all employees.
- If no person is found with the first name, last name or id, an error generated with the constructor function **Error** of the standard JavaScript library with the message **"Invalid information"** should be raised.
- Upon receiving the options object with the name property, it looks for the corresponding employee person;
- The name option must accept first and last name to perform the search.
