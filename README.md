# gson-threeten-serialisers

## What is it?

A set of [GSON][1] serialiser/deserialisers for dealing with [Java 7 "three ten" backport of the `java.time` entities][2].  Wherever possible, [ISO 8601 string representations](http://en.wikipedia.org/wiki/ISO_8601) are used.  

Note: if you are using Java 8 then you're in the wrong place - use the [gson-javatime-serialisers][3] instead.

## Getting it

*(Details to be included once released to Maven Central)*

## Using it

````
final Gson gson = Converters.registerOffsetDateTime(new GsonBuilder()).create();
final OffsetDateTime original = OffsetDateTime.now();

final String json = gson.toJson(original);
final OffsetDateTime reconstituted = gson.fromJson(json, OffsetDateTime.class);
````


[1]: https://code.google.com/p/google-gson/
[2]: http://www.threeten.org/threetenbp/
[3]: https://github.com/gkopff/gson-javatime-serialisers
