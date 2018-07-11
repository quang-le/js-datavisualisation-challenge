**Challenge Javascript Solo: Datavisualisation**
*created by quang-le on 09/07/2018*
*Last update 09/07/2018*


1. Introduction
* Challenge objectives: 
    - DOM manipulation
    - AJAX requests
    - Use of 3rd party libraries (in this case d3/Dimple)
    - Problem-solving
    - Debugging using the console
    - Understand prioritizing

* The challenge:
Before the end of the week:
    - Insert 2 interactive graphic representations of html tables (file provided)
    - Insert a table using data fetched through an AJAx request with an update every second.
    [Full instructions in French](https://github.com/becodeorg/lovelace-2/tree/master/Projects/javascript-challenge-solo)

2. Planning
* Determine benchmark for either task (minimum to achieve and best case result) - OK 09/07/2018, 10:47
* Code the AJAX request, with minimum formatting - Done 09/07/2018, 11:00. Server problem pending coach's side.
* Find place in the DOM to insert the graphs - OK 09/07/2018, 09:30 (during review)
* If possible at this stage, make basic DOM insertion - OK 09/07/2018, 11:50: inserted text. 
* Choose between Dimple and D3 
* Learn to use the library
* Create branch for low-tier result
* Implement low-tier result
* If time allows it: repeat with high-tier result.


3. Determine 2 tiers of expected results

X. Log 
09/07/2018: 
- create AJAX request: html error 0. Request blocked server side. Leave it a that for now. The script seems to work properly though. Error identification process: console logged the request lauching, then an error message, then the other steps of the request (reached state 4, then failed then logged html error 0)
- 14:00: put the page on github page as the console logged many errors saying http or https protocol was required. Moving the stable version of the project to the dev branch.
- 14:30: manage to change inner HTML at the right place but dimple doesn't seem to work as intended; Then again I just copied and pasted the example. Time to dive deeper in the library. 
- 15:00: checked the AJAX request with the new url provided.It works.
- 15:30: figured out the example used a .tsv file but an array of object could be used instead
- 16:30: installed jQuery and used selectors to find a (legible) way to target the data to be looped through
- 17:30: fixed the loop that creates the array containing the data in the html
- 17:35: Dimple seems to create the same problems as working with a css template. Might as well work directly in d3. 
- 18:20: made the graph work with Dimple. The data in html needed to be modified, so that the comma in the numbers is replaced by a dot, in order to be able to `parseFloat` the data. Remaining bugs: no grapgh generated for countries with incomplete data sets (France, Ireland), need to crop the names of countries with footnote reference (eg: Turkey). Also: a readable unit scale is needed for y-axis.

10/07/2018:
- 12:00: read d3 tutorials. Feeling ready to try something out.
- 12:05: merged dimple graphs on master. Created d3 branch
- 17:00: somehow all changes were carried on to master. Couldn't make enough sense od D3 documantation

11/07/2018:
- 10:30: found good resource online. 
- 14:00: finished reading online book about D3
- 14:30: start reviewing planned graph, switching to bar graph, with a twist TBD.
- 15:30: start coding new bar graph


