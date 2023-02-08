# Name

`-name` Command is used to find the file with the name that is provided and the path that the file leads to

## Example 1:

`find skill-demo1-data/written_2/ -name HandRHawaii.txt
skill-demo1-data/written_2/travel_guides/berlitz1/HandRHawaii.txt`

One can enter the Command to find HandRHawaii.txt and have it return the path to the file named HandRHawaii.txt that was requested.

## Example 2:

`find skill-demo1-data/written_2/ -name Bahamas-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-History.txt`

One can enter the Command to find Bahamas-History.txt and it returns the path to the file named Bahamas-History.txt that was requested.

<div></div>

<div></div>

# Empty

`-empty` Command is used to find the file(s) that are empty in the directory that was provided

## Example 1:

Once can create an empty file in `skill-demo1-server/skill-demo1-data/written_2/travel_guides/berlitz1` called emptyFile.txt. The command will find the file path. The path was returned.

`find skill-demo1-server/skill-demo1-data/written_2/ -empty
skill-demo1-server/skill-demo1-data/written_2/travel_guides/berlitz1/emptyFile.txt`

## Example 2:

The emptyFile that was created earlier was removed and this command was run and returned nothing.

`find skill-demo1-data/written_2/ -empty`

<div></div>

<div></div>

find skill-demo1-data/written_2/ -name sample.txt -exec rm -i {} \; 
rm: remove regular empty file 'skill-demo1-data/written_2/travel_guides/berlitz1/sample.txt'? y
<div></div>
<img width="821" alt="Screenshot 2023-02-08 at 2 00 58 PM" src="https://user-images.githubusercontent.com/43663025/217660993-6cfde5cf-370a-4320-835b-f9097f44275c.png">

[cs15lwi23aio@ieng6-202]:skill-demo1-server:507$ find skill-demo1-data/written_2/ -name WhereToLosAngeles.txt -exec rm -i {} \; 
rm: remove regular file 'skill-demo1-data/written_2/travel_guides/berlitz1/WhereToLosAngeles.txt'? y
<div></div>
<img width="900" alt="Screenshot 2023-02-08 at 2 02 24 PM" src="https://user-images.githubusercontent.com/43663025/217661218-1a52891c-fc07-4058-9f61-9efc986dacb6.png">


<div></div>

[cs15lwi23aio@ieng6-202]:skill-demo1-server:516$ find skill-demo1-data/written_2/ -type f -name "*.txt" -exec grep 'San Fernando Valley'  {} \;
        gift stores. Just north of Los Angeles, the San Fernando Valley’s main
        in the San Fernando Valley, opening in 2004, and one in Little Tokyo,
The great mass of Los Angeles’s population lives in the sprawling suburbs of the valleys — the San Fernando Valley north of the Hollywood Hills and the San Gabriel Valley stretching east towards San Bernardino. It’s composed mainly of suburbs and uninspired strip centers (block-long low-rise shopping malls), but there are a few reasons to drop by.
One of the most enjoyable is a tour of the film and television studios located in the San Fernando Valley. Two major TV networks — CBS and NBC — welcome you onto their sets for a look behind the scenes at some of America’s most popular TV shows. A limited number of tickets to live shows are available. Universal Studios Hollywood, just north of the Hollywood Freeway (either the Universal Center Drive or the Lankershim Boulevard exits), offers an elaborate tour in open trams. In the course of displays of special-effects trickery you’ll be attacked by the shark from Jaws, meet up with a three-story-tall King Kong, and be subjected to all the earthquakes, floods, and fires you ever saw in a disaster movie. You can also take a look behind the scenes and learn about techniques that are used to create film’s great illusions. The highlight is the Back To The Future ride. Seated in a flight simulator shaped like the famous time-traveling DeLorean car in the films, you will be taken on a hair-raising chase through time and space.
[cs15lwi23aio@ieng6-202]:skill-demo1-server:517$ 

[cs15lwi23aio@ieng6-202]:skill-demo1-server:517$ find skill-demo1-data/written_2/ -type f -name "*.txt" -exec grep 'Orange County'  {} \;
        area and Orange County. All hotels are of a high standard, with private
        Galleria and nearby Fashion Square. Orange County residents rejoice
        another good Orange County shopping enclave.
        available in Orange County as well as in the desert communities in and
        Orange County is one big water playground. Beaches from Long Beach to
        Orange County, Newport Beach is a major center for rentals, and so is
        Orange County is Laguna Beach, as the entire city beach area is a
        various South Bay beaches — as well as those in Orange County — have
L.A. covers such an immense area that the first-time visitor can easily feel overwhelmed. The best way to approach the city is to break it down into smaller regions and then take them one at a time — Downtown, Hollywood, Westside, the Coast, the Valleys, and Orange County.
Orange County
Orange County, bedrock of conservative Southern California, is the birthplace of ex-president Richard Nixon, and land of the lawn sprinkler, the two-car garage, and the “planned community.” Along the coast, however, you can rediscover the beach culture that gave birth to the Beach Boys, and at Anaheim you can indulge yourself in the delights of California’s number-one tourist attraction.

The URL: https://www.geeksforgeeks.org/find-command-in-linux-with-examples/
