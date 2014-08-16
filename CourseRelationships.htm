

<!DOCTYPE html>
<html>
<meta charset="utf-8">
<title>Data Science Course Dependencies</title>
<style>
#chart {
	height: 500px;
}

.node rect {
	cursor: move;
	fill-opacity: .9;
	shape-rendering: crispEdges;
}

.node text {
	pointer-events: none;
	text-shadow: 0 1px 0 #fff;
}

.link {
	fill: none;
	stroke: #000;
	stroke-opacity: .2;
}

.link:hover {
	stroke-opacity: .5;
}

#chart svg {
	background-color: #ffffee; 
}
</style>
<body>

<header>
	<h1>Data Science Course Dependencies</h1>
</header>

<p id="chart"></p>

<aside>Drag to rearrange nodes.</aside>

<aside>Thanks to Mike Bostock for the <a href="http://d3js.org/">d3 library</a> and Tom Counsell for the <a href="http://tamc.github.com/Sankey/">Sankey library</a>.</aside>


<script src="js/d3.v2.min.2.9.1.js"></script>
<script src="sankey.js"></script>
<script>

var margin = {top: 1, right: 1, bottom: 6, left: 1},
    width = 960 - margin.left - margin.right,
    height = 500 - margin.top - margin.bottom;

var format = function(d) { return d == 1 ? "Soft Requirement" : "Hard Requirement"; },
    color = d3.scale.category20();

var svg = d3.select("#chart").append("svg")
	.attr("width", width + margin.left + margin.right)
	.attr("height", height + margin.top + margin.bottom)
	.append("g")
	.attr("transform", "translate(" + margin.left + "," + margin.top + ")");

var sankey = d3.sankey()
	.nodeWidth(15)
	.nodePadding(10)
	.size([width, height / 2]);

var path = sankey.link();

d3.json("DataScience2.json", function(ds) {
	sankey
		.nodes(ds.nodes)
		.links(ds.links)
		.layout(32);
	
	var link = svg.append("g").selectAll(".link")
		.data(ds.links)
		.enter().append("path")
		.attr("class", "link")
		.attr("d", path)
		.style("stroke-width", function(d) { return Math.max(1, d.dy); })
		.sort(function(a, b) { return b.dy - a.dy; });
	
	link.append("title")
		.text(function(d) { return d.source.name + " → " + d.target.name + "\n" + format(d.value); });
	
	var node = svg.append("g").selectAll(".node")
		.data(ds.nodes)
		.enter().append("g")
		.attr("class", "node")
		.attr("transform", function(d) { return "translate(" + d.x + "," + d.y + ")"; })
		.call(d3.behavior.drag()
			.origin(function(d) { return d; })
			.on("dragstart", function() { this.parentNode.appendChild(this); })
			.on("drag", dragmove));
	
	node.append("rect")
		.attr("height", function(d) { return d.dy; })
		.attr("width", sankey.nodeWidth())
		.style("fill", function(d) { return d.color = color(d.name.replace(/ .*/, "")); })
		.style("stroke", function(d) { return d3.rgb(d.color).darker(2); })
		.append("title")
		.text(function(d) { return d.name + "\n"; });
	
	node.append("text")
		.attr("x", -6)
		.attr("y", function(d) { return d.dy / 2; })
		.attr("dy", ".35em")
		.attr("text-anchor", "end")
		.attr("transform", null)
		.text(function(d) { return d.name; })
		.filter(function(d) { return d.x < width / 2; })
		.attr("x", 6 + sankey.nodeWidth())
		.attr("text-anchor", "start");
	
	function dragmove(d) {
		d3.select(this).attr("transform", "translate(" + d.x + "," + (d.y = Math.max(0, Math.min(height - d.dy, d3.event.y))) + ")");
		sankey.relayout();
		link.attr("d", path);
	}
});
</script>
