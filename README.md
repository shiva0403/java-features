Java 17 features

1) Records
2) Switch Expressions
3) Text Blocks
4) Pattern Matching

Record 

Eliminates boiler plate code
Works like a class

Example

public record State(String name, Stiring abbr) {}

Ex:
new State("Washington DC", "DC")

Text blocks

Eliminates line breaks
Useful for configuation and json

Example:

String response = """
            {
                "state": {
                    "name": "Washington DC",
                    "abbrev": "DC"
                }
            }
                """;

Switch Expressions:

Month month = Month.JUNE;
var result = switch(month) {
    case JANUARY, MARCH, MAY, JULY, SEPTEMBER, NOVEMBER -> "odd";
    case FEBRUARY, APRIL, JUNE, AUGUST, OCTOBER, DECEMBER -> "even";
    default -> "neither";
};
system.out.println("Month: " + result);
}

Pattern Matching:
instanceof operator is not required
eliminates casts

Webservice service = new DbService();
switch(service) {
    case DbService db -> System.out.println("db call");
    case RestfulService rest -> System.out.println("web service call");
}
