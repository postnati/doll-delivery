You are a nice old lady who delivers porcelain dolls on foot using your walker to residents in a neighborhood. Every day a nice young man fills your handbag with porcelain dolls. He gives you a map of the neighborhood and an address of the neighbor to deliver the handbag of dolls to. The handbag is extremely heavy and you have a bad hip so you always try to minimize the walking distance from your beginning position to your destination. Your job is to determine the shortest path to take to deliever your handbag of dolls.

**Write a function in the [Scala](http://www.scala-lang.org/) programming language** when given:

* a starting location
* a target location
* a list of edges where each edge is represented as a map and connects two locations
  
Produces the shortest path with distance which:

* starts at the given starting location
* ends at the given target location
 
Include a set of executable high-level tests for your solution. The following is a set of inputs for which the correct result is known:

![Neighborhood Map](https://raw.github.com/postnati/doll-delivery/master/neighborhood-map.png)

Input:

    startingLocation: "Kruthika's abode"

    targetLocation: "Craig's haunt"

    edges: 

    List(
      Map("startLocation" -> "Kruthika's abode", "endLocation" -> "Mark's crib", "distance" -> 9),
      Map("startLocation" -> "Kruthika's abode", "endLocation" -> "Greg's casa", "distance" -> 4),
      Map("startLocation" -> "Kruthika's abode", "endLocation" -> "Matt's pad", "distance" -> 18),
      Map("startLocation" -> "Kruthika's abode", "endLocation" -> "Brian's apartment", "distance" -> 8),
      Map("startLocation" -> "Brian's apartment", "endLocation" -> "Wesley's condo", "distance" -> 7),
      Map("startLocation" -> "Brian's apartment", "endLocation" -> "Cam's dwelling", "distance" -> 17),
      Map("startLocation" -> "Greg's casa", "endLocation" -> "Cam's dwelling", "distance" -> 13),
      Map("startLocation" -> "Greg's casa", "endLocation" -> "Mike's digs", "distance" -> 19),
      Map("startLocation" -> "Greg's casa", "endLocation" -> "Matt's pad", "distance" -> 14),
      Map("startLocation" -> "Wesley's condo", "endLocation" -> "Kirk's farm", "distance" -> 10),
      Map("startLocation" -> "Wesley's condo", "endLocation" -> "Nathan's flat", "distance" -> 11),
      Map("startLocation" -> "Wesley's condo", "endLocation" -> "Bryce's den", "distance" -> 6),
      Map("startLocation" -> "Matt's pad", "endLocation" -> "Mark's crib", "distance" -> 19),
      Map("startLocation" -> "Matt's pad", "endLocation" -> "Nathan's flat", "distance" -> 15),
      Map("startLocation" -> "Matt's pad", "endLocation" -> "Craig's haunt", "distance" -> 14),
      Map("startLocation" -> "Mark's crib", "endLocation" -> "Kirk's farm", "distance" -> 9),
      Map("startLocation" -> "Mark's crib", "endLocation" -> "Nathan's flat", "distance" -> 12),
      Map("startLocation" -> "Bryce's den", "endLocation" -> "Craig's haunt", "distance" -> 10),
      Map("startLocation" -> "Bryce's den", "endLocation" -> "Mike's digs", "distance" -> 9),
      Map("startLocation" -> "Mike's digs", "endLocation" -> "Cam's dwelling", "distance" -> 20),
      Map("startLocation" -> "Mike's digs", "endLocation" -> "Nathan's flat", "distance" -> 12),
      Map("startLocation" -> "Cam's dwelling", "endLocation" -> "Craig's haunt", "distance" -> 18),
      Map("startLocation" -> "Nathan's flat", "endLocation" -> "Kirk's farm", "distance" -> 3)
    )

Result:
  
    Map("distance" -> 31, "path" -> "Kruthika's abode => Brian's apartment => Wesley's condo => Bryce's den => Craig's haunt")

Hints:

* read about [Dijkstra's Algorithm](http://en.wikipedia.org/wiki/Dijkstra%27s_algorithm)
* find more interesting example data for test cases on the internet
