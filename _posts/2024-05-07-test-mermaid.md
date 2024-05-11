---
layout: default

title:  Mermaid
tags: [term]
use_mermaid: true
---

<html>
<body>
	
<h2>Mermaid graph diagram:</h2>
<table><tr>
<td>
<pre>
graph TD 
A[Client] --> B[Load Balancer] 
B --> C[Server1] 
B --> D[Server2]
</pre>
</td>
<td>
<pre class="mermaid">
	graph TD 
	A[Client] --> B[Load Balancer] 
	B --> C[Server1] 
	B --> D[Server2]
 </pre>
</td>
<td><pre>
   graph TD 
	A[Client] -->|tcp_123| B
	B(Load Balancer) 
	B -->|tcp_456| C[Server1] 
	B -->|tcp_456| D[Server2]
</pre></td>
<td>
<pre class="mermaid">
	graph TD 
	A[Client] -->|tcp_123| B
	B(Load Balancer) 
	B -->|tcp_456| C[Server1] 
	B -->|tcp_456| D[Server2]
 </pre>
</td>
</tr></table>

<h2>Basic flowchart</h2>
<table><tr><td>
<pre>
graph LR
    A[Square Rect] -- Link text --> B((Circle))
    A --> C(Round Rect)
    B --> D{Rhombus}
    C --> D
</pre>
</td><td>
<pre class="mermaid">
graph LR
    A[Square Rect] -- Link text --> B((Circle))
    A --> C(Round Rect)
    B --> D{Rhombus}
    C --> D
</pre>
</td></tr></table>

<h2>Basic flowchart 2</h2>
<table><tr><td>
<pre>
graph TB
    A[Square Rect] -- Link text --> B{Rhombus}
    B -->C
    B --> D{Rhombus}
    D --> E
    D --> F
    D --> G
</pre>
</td><td>
<pre class="mermaid">
graph TB
    A[Square Rect] -- Link text --> B{Rhombus}
    B -->C
    B --> D{Rhombus}
    D --> E
    D --> F
    D --> G
</pre>
</td></tr></table>


<h2>Timeline Example</h2>
<table><tr><td>
<pre>timeline
    title History of Social Media Platform
    2002 : LinkedIn
    2004 : Facebook
         : Google
    2005 : Youtube
    2006 : Twitter
</pre>
</td><td>
 <pre class="mermaid">
timeline
    title History of Social Media Platform
    2002 : LinkedIn
    2004 : Facebook
         : Google
    2005 : Youtube
    2006 : Twitter
	</pre>
</td></tr></table>

<h2>Pie chart:</h2>
<table><tr><td>
<pre>	
pie title NETFLIX
	 "Time spent looking for movie" : 90
	 "Time spent watching it" : 10
</pre>
</td><td>
 <pre class="mermaid">
pie title NETFLIX
	 "Time spent looking for movie" : 90
	 "Time spent watching it" : 10
</pre>
</td></tr></table>

<h2>Mindmap Diagram</h2>
<table><tr><td>
<pre>
mindmap
  root((mindmap))
    Origins
      Long history
      ::icon(fa fa-book)
      Popularisation
        British popular psychology author Tony Buzan
    Research
      On effectiveness<br/>and features
      On Automatic creation
        Uses
            Creative techniques
            Strategic planning
            Argument mapping
    Tools
      Pen and paper
      Mermaid
</pre>
</td><td>
<pre class="mermaid">
mindmap
  root((mindmap))
    Origins
      Long history
      ::icon(fa fa-book)
      Popularisation
        British popular psychology author Tony Buzan
    Research
      On effectiveness<br/>and features
      On Automatic creation
        Uses
            Creative techniques
            Strategic planning
            Argument mapping
    Tools
        Pen and paper
        Mermaid
</pre>
</td></tr></table>

<h2>Requirement Diagram</h2>
<table><tr><td>
<pre>
    requirement test_req {
    id: 1
    text: the test text.
    risk: high
    verifymethod: test
    }

    element test_entity {
    type: simulation
    }

    test_entity - satisfies -> test_req
</pre>
</td><td>
<pre  class="mermaid">
requirementDiagram
    requirement test_req {
    id: 1
    text: the test text.
    risk: high
    verifymethod: test
    }

    element test_entity {
    type: simulation
    }

    test_entity - satisfies -> test_req
</pre>
</td></tr></table>

<h2>Complete flowchart</h2>
<table><tr><td>
<pre>
Left to right(LR) graph orientation :
(options:
TB - top to bottom
TD - top-down/ same as top to bottom
BT - bottom to top
RL - right to left
LR - left to right )

graph LR
    A[Square Rect] -- Link text --> B((Circle))
    A --> C(Round Rect)
    B --> D{Rhombus}
    C["`**Markdown** string`"] --> D
	E -->F([Stadium-shaped node]}
	id1[[This is  subroutine shape]]
	id2[(Database)]
	id3((This is the text in the circle))
	id4 >asymmetric shape]
	id5{decision} 
	id6{{Hexagon}}
	id7[/Parallelogram/] 
	id8(((Double circle)))
	F-.->dottedLink;
	G-.dotted link with text .->H
	H == thick link ==> I
	J -- text --> K -- chaining link --> L
	M --o N
    N --x O
	O x--x P
</pre>
</td><td>
<pre class="mermaid">
graph LR
    A[Square Rect] -- Link text --> B((Circle))
    A --> C(Round Rect)
    B --> D{Rhombus}
    C --> E["`**Markdown** string`"] 
	E -->F([Stadium-shaped node])
	id1[[This is subroutine shape]]
	id2[(Database)]
	id3((This is the text in the circle))
	id4>asymmetric shape]
	id5{decision}
	id6{{Hexagon}}	
	id7[/Parallelogram/]
	id8(((Double circle)))
	F-.->dottedLink;
	G-.dotted link with text .->H
	H == thick link ==> I
	J -- text --> K -- chaining link --> L
	M --o N
    N --x O
	O x--x P
	
</pre>
</td></tr></table>

<h2>real flowchart</h2>
<table><tr><td>
<pre>
flowchart TD
    A[Start] --> B{Is it?}
    B -->|Yes| C[OK]
    C --> D[Rethink]
    D --> B
    B ---->|No| E[End]

</pre>
</td><td>
<pre class="mermaid">
flowchart TD
%% this is a comment : TD means top down orientation of the chart
    A[Start] --> B{Is it?}
    B -->|Yes| C[OK]
    C --> D[Rethink]
    D --> B
    B ---->|No| E[End]

</pre>
</td></tr></table>

<h2>Styling</h2>
<table><tr><td>
<pre>
flowchart LR
    id1(Start)-->id2(Stop)
    style id1 fill:#f9f,stroke:#333,stroke-width:4px
    style id2 fill:#bbf,stroke:#f66,stroke-width:2px,color:#fff,stroke-dasharray: 5 5
</pre>
<pre  class="mermaid">
flowchart LR
    id1(Start)-->id2(Stop)
    style id1 fill:#f9f,stroke:#333,stroke-width:4px
    style id2 fill:#bbf,stroke:#f66,stroke-width:2px,color:#fff,stroke-dasharray: 5 5
</pre>
</td></tr></table>

<h2>Applying CSS classes</h2>
<table><tr><td>
<pre>
<!-- predefine class -->
<style>
  .cssClass > rect {
    fill: #ff0000;
    stroke: #ffff00;
    stroke-width: 4px;
	font-size:20px;
  }
</style>
code:
flowchart LR
    A-->B[AAA<span>BBB</span>]
    B-->D
    class A cssClass
</pre>
<style>
  .mycssClass  {
    font-size:20px;
  }
</style>
<pre  class="mermaid">
%%{init: {"flowchart": {"defaultRenderer": "elk"}} }%%
flowchart LR
    A-->B[AAA<span>BBB</span>]
    B-->D
    class A mycssClass
</pre>
</td></tr></table>

<!-------------------------------------------------------------------------------------->
</body>

<!--
<script type="module">
      import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
      mermaid.initialize({ startOnLoad: true });
</script>
-->

</html>