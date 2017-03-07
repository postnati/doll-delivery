You are a nice old lady who delivers porcelain dolls on foot using your walker to residents in a neighborhood. Every day a nice young man fills your handbag with porcelain dolls. He gives you a map of the neighborhood and an address of the neighbor to deliver the handbag of dolls to. The handbag is extremely heavy and you have a bad hip so you always try to minimize the walking distance from your beginning position to your destination. Your job is to determine the shortest path to take to deliever your handbag of dolls.

**Write a function in the [Kotlin](http://kotlinlang.org/) programming language** when given:

* a starting location
* a target location
* a list of edges where each edge is represented as a map and connects two locations
  
Produces the shortest path with distance which:

* starts at the given starting location
* ends at the given target location
 
The function should have a signature like this:

    fun dijkstra(startLocation: String, endLocation: String, edges: List<Map<String, String>>): Map<String, String>

where an `edge` is a `Map` with keys for `startLocation`, `endLocation`, and `distance`. The return value should be a `Map` with keys for `distance` and `path`.

Include a set of executable high-level tests for your solution. The following is a set of inputs for which the correct result is known:

![Neighborhood Map](https://raw.github.com/postnati/doll-delivery/master/neighborhood-map.png)

Input:

    dijkstra(
      startingLocation = "Kruthika's abode",
      targetLocation = "Craig's haunt",
      edges = 
        listOf(
          mapOf("startLocation" to "Kruthika's abode", "endLocation" to "Mark's crib", "distance" to 9),
          mapOf("startLocation" to "Kruthika's abode", "endLocation" to "Greg's casa", "distance" to 4),
          mapOf("startLocation" to "Kruthika's abode", "endLocation" to "Matt's pad", "distance" to 18),
          mapOf("startLocation" to "Kruthika's abode", "endLocation" to "Brian's's apartment", "distance" to 8),
          mapOf("startLocation" to "Brian's apartment", "endLocation" to "Wesley's condo", "distance" to 7),
          mapOf("startLocation" to "Brian's apartment", "endLocation" to "Cam's dwelling", "distance" to 17),
          mapOf("startLocation" to "Greg's casa", "endLocation" to "Cam's dwelling", "distance" to 13),
          mapOf("startLocation" to "Greg's casa", "endLocation" to "Mike's digs", "distance" to 19),
          mapOf("startLocation" to "Greg's casa", "endLocation" to "Matt's pad", "distance" to 14),
          mapOf("startLocation" to "Wesley's condo", "endLocation" to "Kirk's farm", "distance" to 10),
          mapOf("startLocation" to "Wesley's condo", "endLocation" to "Nathan's flat", "distance" to 11),
          mapOf("startLocation" to "Wesley's condo", "endLocation" to "Bryce's den", "distance" to 6),
          mapOf("startLocation" to "Matt's pad", "endLocation" to "Mark's crib", "distance" to 19),
          mapOf("startLocation" to "Matt's pad", "endLocation" to "Nathan's flat", "distance" to 15),
          mapOf("startLocation" to "Matt's pad", "endLocation" to "Craig's haunt", "distance" to 14),
          mapOf("startLocation" to "Mark's crib", "endLocation" to "Kirk's farm", "distance" to 9),
          mapOf("startLocation" to "Mark's crib", "endLocation" to "Nathan's flat", "distance" to 12),
          mapOf("startLocation" to "Bryce's den", "endLocation" to "Craig's haunt", "distance" to 10),
          mapOf("startLocation" to "Bryce's den", "endLocation" to "Mike's digs", "distance" to 9),
          mapOf("startLocation" to "Mike's digs", "endLocation" to "Cam's dwelling", "distance" to 20),
          mapOf("startLocation" to "Mike's digs", "endLocation" to "Nathan's flat", "distance" to 12),
          mapOf("startLocation" to "Cam's dwelling", "endLocation" to "Craig's haunt", "distance" to 18),
          mapOf("startLocation" to "Nathan's flat", "endLocation" to "Kirk's farm", "distance" to 3)
        ))

Result:
  
    {"distance" = 31, "path" = "Kruthika's abode => Brian's apartment => Wesley's condo => Bryce's den => Craig's haunt"}

Hints:

* read about [Dijkstra's Algorithm](http://en.wikipedia.org/wiki/Dijkstra%27s_algorithm)
* find more interesting example data for test cases on the internet

We strongly recommend using IntelliJ to work with Kotlin. You can find details about [setting up IntelliJ here](https://kotlinlang.org/docs/tutorials/getting-started.html).
