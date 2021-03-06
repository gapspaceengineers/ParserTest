# APX market data parser

* **date** ("date_applied" in JSON) - Date as milliseconds since start of epoch (start of day). Timezone seems to be Netherlands standard (with daylight saving).
* **hour** - based on either "Order" or "Hour" field, we need to figure out the hour-of-day for which particular data row is applicable for.
* **net volume** - use the value from "Net Volume" field
* **price** - use the value from "Price" field

For JSON parsing, we use [Jackson](https://github.com/FasterXML/jackson).

### Basic steps

* Define object model in Java (classes `QuoteResponse`, `Quote`, `QuoteValue`).
* Implement code to parse JSON into the object model.
* Implement unit test for the code (load sample from class path, verify it was parsed correctly).

### Building

You can use either Gradle, Gradle wrapper or Maven
