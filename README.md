# Turkey Cities and Districts Data

This repository provides a comprehensive dataset of Turkish cities (iller) and districts (ilçeler) sourced from the Mernis database. The data is available in multiple formats for easy integration into your projects.

## Data Formats

* **JSON:** `turkey_cities_districts.json` - A structured JSON file containing the hierarchical relationship between cities and their districts. Ideal for use in JavaScript, Python, and other applications.
* **SQL:** `turkey_cities_districts.sql`
    * **Table Schema:** Creates a SQL table to store the city and district data.
    * **Value Inserts:** Includes SQL `INSERT` statements to populate the table with the data.
    * **Value List:** Provides a simple list of all districts, suitable for use in dropdowns or selection lists.

## Usage

### JSON

You can directly access the JSON data by making a request to the following [URL](https://furkandlkdr.github.io/mernis-turkiye-disctricts/turkey_cities_districts.json).
This will return the complete JSON dataset of Turkish cities and districts.

```javascript
// Example using JavaScript (Fetch API)
fetch('[https://furkandlkdr.github.io/mernis-turkiye-disctricts/turkey_cities_districts.json](https://furkandlkdr.github.io/mernis-turkiye-disctricts/turkey_cities_districts.json)')
  .then(response => response.json())
  .then(data => {
    // Process the data here
    console.log(data.cities[0].name); // Output: "Adana"
  });
```
### SQL

Execute the turkey_cities_districts.sql file in your SQL environment to create the table and insert the data.
Use standard SQL queries to interact with the data:

```SQL
SELECT * FROM City WHERE City = 'İstanbul';
SELECT * FROM District WHERE District Name = 'Beşiktaş';
```

### Data Structure (JSON)

```javascript
{
    "1": {
        "province": "Adana",
        "districts": [
            {
                "id": 1757,
                "name": "Aladağ"
            },
            {
                "id": 1219,
                "name": "Ceyhan"
            },
            //...
        ]
    },
    "2": {
        "province": "Adıyaman",
        "districts": [
            {
                "id": 1182,
                "name": "Besni"
            },
            {
                "id": 1246,
                "name": "Çelikhan"
            },
            //...
    },
    ///...
}
```

### Contributing

If you find any inaccuracies or have updates to the data, please feel free to submit a pull request.

`Search engine texts: Türkiye ilçe listesi, Türkiye iller listesi, Turkiye District List, Turkiye District, Turkiye Provinces`
