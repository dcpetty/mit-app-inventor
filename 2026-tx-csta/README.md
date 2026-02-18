# 2026-tx-csta

## About these apps

These apps are starter [MIT App Inventor](http://ai2.appinventor.mit.edu/) apps as presented at the [2026 Texas CSTA Regional Conference](https://docs.google.com/document/d/1s8OYp63AiIemV9x0erBY7EYnq_CWUQXRzCJBEfejxKU/). The slides accompanying this presentation are available at [https://aif.to/2026-tx-csta](https://aif.to/2026-tx-csta).

## Apps

| App | .AIA | Description |
| --- | --- | --- |
| Doodle | <a href="https://code.appinventor.mit.edu/?repo=https://raw.githubusercontent.com/dcpetty/mit-app-inventor/refs/heads/main/2026-tx-csta/DoodleStarter.aia"><img src="../codi-32x32.png" alt="codi" style="vertical-align: middle;"><code>DoodleStarter.aia</code></a> | A basic drawing app. |
| Map | <a href="https://code.appinventor.mit.edu/?repo=https://raw.githubusercontent.com/dcpetty/mit-app-inventor/refs/heads/main/2026-tx-csta/MapStarter.aia"><img src="../codi-32x32.png" alt="codi" style="vertical-align: middle;"><code>MapStarter.aia</code></a> | A basic mapping app that calculates ([great circle](https://en.wikipedia.org/wiki/Great_circle)) distances between locations. |
| GoodReader | <a href="https://code.appinventor.mit.edu/?repo=https://raw.githubusercontent.com/dcpetty/mit-app-inventor/refs/heads/main/2026-tx-csta/GoodReaderStarter.aia"><img src="../codi-32x32.png" alt="codi" style="vertical-align: middle;"><code>GoodReaderStarter.aia</code></a> | Use a generative artificial intelligence [ChatBot](https://gemini.google.com/app) to encourage critical reading skills. |
| Journal | <a href="https://code.appinventor.mit.edu/?repo=https://raw.githubusercontent.com/dcpetty/mit-app-inventor/refs/heads/main/2026-tx-csta/JournalStarter.aia"><img src="../codi-32x32.png" alt="codi" style="vertical-align: middle;"><code>JournalStarter.aia</code></a> | A basic journal app crowd-sourced data in a shared [Google Sheet](https://docs.google.com/spreadsheets/d/16-hA2pixAtVlUXWVXWUHK21pBuEiZXZhDDnSW-uHg7E/). |

## Projects

The [MIT App Inventor](http://ai2.appinventor.mit.edu/) block code for the completed apps is below.

<style>
table { width: 100%; }
li { list-style-type: square; font-size: small; }
span { background-color: #bcdb74; border-radius: 8px; padding: 2px 6px; }
</style>

### Doodle

#### What we learned

<table><tr>

<td>

<h5>From the starter project in the <span>Designer</span></h5>
<ul>
<li><em>Screen1</em> is set to <code>Title: Doodle</code> &mdash; as are all project titles.</li>
<li><em>Canvas1</em> is set to <code>Width: Fill Parent...</code> and <code>Height: Fill Parent...</code> to fill out the <em>Screen1</em> extent.</li>
<li><em>HorizontalArrangement1</em> is set to <code>Visible: &#x2610;</code> rendering it invisible.</li>
<li><em>HorizontalArrangement1</em> is set to <code>Width: Fill Parent...</code> for when it is made visible.</li>
</ul> 

</td>

<td>

<h5>From the completed project in the <span>Designer</span></h5>
<ul>
<li><em>HorizontalArrangement1</em> is set to <code>Visible: &#x2612;</code> rendering it visible.</li>
<li><em>ButtonClear</em> is added to <em>HorizontalArrangement1</em>, renamed, and set to <code>Text: Clear</code>.</li>
<li><em>SliderWidth</em> is added to <em>HorizontalArrangement1</em>, renamed, and set to <code>Width: Fill Parent...</code>, <code>MaxValue: 20</code>, <code>MinValue: 2</code>, <code>NumberOfSteps: 18</code>, <code>ThumbPosition: 2</code>.</li>
</ul> 

<h5>From the completed project in the <span>Blocks</span></h5>
<ul>
<li>The <em>Canvas1.Dragged</em> event calls <em>Canvas1.DrawLine</em> with the proper <a href="https://ai2.appinventor.mit.edu/reference/components/animation.html#Canvas">parameters</a>.</li>
<li>The <em>ButtonClear.Clicked</em> event calls <em>Canvas1.Clear</em>.</li>
<li>The <em>SliderWidth.PositionChanged</em> sets <em>Canvas1.LineWidth</em> to the <code>thumbPosition</code> parameter value.</li>
</ul> 

</td>

</tr></table>

#### Code

<img src="./Doodle-blocks.png" alt="Doodle blocks">

### Map

#### What we learned

<table><tr>

<td>

<h5>From the starter project in the <span>Designer</span></h5>
<ul>
<li><em>Screen1</em> is set to <code>Title: Map</code> &mdash; as are all project titles.</li>
<li><em>Map1</em> is set to <code>Width: Fill Parent...</code> and <code>Height: Fill Parent...</code> to fill out the <em>Screen1</em> extent.</li>
<li><em>MarkerMcMillen</em> is set to <code>FillColor: Blue</code> (because the default is <code>Red</code>), <code>Latitude: 33.028</code> (the latitude of <a href="https://mcmillen.pisd.edu/">McMillen High School</a>, <code>Longitude:  -96.611</code> (the longitude of <a href="https://mcmillen.pisd.edu/">McMillen High School</a>), and <code>Draggable: &#x2610;</code> (so the marker will remain fixed).</li>
</ul> 

</td>

<td>

<h5>From the completed project in the <span>Blocks</span></h5>
<ul>
<li>The <em>Map1.LongPressAtPoint</em> event initializes the local variable <em>pin</em> with the result of the call to <em>Map1.CreateMarker</em> using the <code>latitude</code> and <code>longitude</code> parameters.</li>
<li>With <em>Any Marker</em> from the <em>Any component</em> drawer, use <em>setMarker.EnableInfoBox</em> with the value of the <em>pin</em> local variable as the <code>of component</code> parameter and <code>true</code> as the <code>to</code> parameter &mdash; thereby enabling the <a href="https://ai2.appinventor.mit.edu/reference/components/maps.html#Map">infobox window display</a> when the user taps the <em>Marker</em>.</li>
<li>With <em>Any Marker</em> from the <em>Any component</em> drawer, use <em>setMarker.Title</em> with the value of the <em>pin</em> local variable as the <code>of component</code> parameter and a <em>Text</em> <em>join</em> of two values as the <code>to</code> parameter: <ul><li>the rounded result of a call to <em>Marker.DistanceToPoint</em> from <em>Any Marker</em> in the <em>Any component</em> drawer with the value of the <em>pin</em> local variable as the <code>of component</code> parameter, the value of the <em>MarkerMcMillen.Latitude</em> property as the <code>latitude</code> parameter, and the value of the <em>MarkerMcMillen.Longitude</em> property as the <code>longitude</code> parameter and;</li><li>the text <code> meters to McMillen</code>.</li></ul></li>
</ul> 

</td>

</tr></table>

#### Code

<img src="./Map-blocks.png" alt="Doodle blocks">

### GoodReader

<img src="./GoodReader-blocks.png" alt="Doodle blocks">

### Journal

<img src="./Journal-blocks.png" alt="Doodle blocks">

<hr>

<div style="display: flex; flex-direction: row; justify-content: space-around; margin: 0 10%;">
<a href="https://dcpetty.github.io/mit-app-inventor/2026-tx-csta/">&#128279; permalink</a> 
<a href="https://github.com/dcpetty/mit-app-inventor/tree/main/2026-tx-csta">&#128230; repository</a>
<!-- 
PERMALINK: https://dcpetty.github.io/mit-app-inventor/REPO/
REPOSITORY: https://github.com/dcpetty/mit-app-inventor/tree/main/REPO
MIT APP INVENTOR: https://code.appinventor.mit.edu/?repo=https://raw.githubusercontent.com/dcpetty/mit-app-inventor/refs/heads/main/REPO/REPO.aia
-->
</div>
