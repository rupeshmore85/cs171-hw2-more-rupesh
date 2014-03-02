Problem 3: Design Critique and Sketching

I. Which graph-related tasks does an ideal GitHub Network Graph need to address?

Solution: An ideal Github Network need to address the below tasks:

1. Nodes : Nodes have an attribute degree that is the number of links
incident to that node.
2. Links : Links can have application specific attribute. Each link
has a direction attribute.
3. Paths : A path is an alternating sequence of nodes and links. If
the links are not weighted, we minimize the number of links in the
path instead.
4. Clusters : A cluster is a set of objects that are spatially closed
together. Subgraphs were elements are connected to each other.
5. Groups : A group can be defined as a set of related nodes, such as
nodes with common attribute values or nodes of interest to users. If
the commits are done by the same user at the same time. Then it can be
grouped
6. Connected component: A connected component is a maximal connected
subgraph. Commit branches can be connected.

Analytical Tasks:

i. Retrieve Value: Given a set of cases, find attributes of those cases.
ii. Filter: Given some conditions on attributes values, find data
cases satisfying those conditions.
iii. Find the extremum : Find data cases possessing an extreme value
of an attribute over its range within the data set.
iv. Sort : Given a set of data, rank them according to some ordinal
metric like commits. Sort the commit points based on the timestamp
v. Determine Range : Given a set of data cases and an attribute of
interest, find the span of values within the set. Determine the range
of commit points to consider for the graph.
vi. Distribution: Given a set of data cases and a quantitative
attribute of interest, characterize the distribution of that
attribute's values over the set.
vii. Find Anomalies: Identify any anomalies within a given set of data
cases with respect to a given relationship or expectation.
viii. Cluster : Given a set of data cases, find clusters of similar
attribute values.
ix. Correlate : Given a set of data cases and two attributes,
determine useful relationships between the values of those attributes.

7. Topology based Tasks:
Adjacency & Accessibility: Set of nodes adjacent to a node for
linking. Accessibility in the sense how many set of nodes are
accessible.
Connectivity: The number of connected components in the graph.

8. Browsing Tasks:
i. Follow a given path: Follow the path between commit points.
ii. Revisit: Return to a previously visited node.

9. Overview Tasks:
To get the estimated values about the size of the graph quickly.

-------------------------------------------------------------------------------------------


II. Get back to the GitHub network visualization you implemented and
test it with the following projects on GitHub: D3, jQuery and
Bootstrap.
There's a lot more data, but the interaction patterns of users are
also very different. What do you notice about the three repositories?

Solution: 

Due to lot of different data, the list of users getting added increases the range of the y axis.
All the 3 mentioned repositories have huge list of contributors than the Caleydo repository.
This gives us more varied range of commit points to link to.
Also the graph becomes a bit messy with huge number of data. A thought need to be given to devise different graph layout 
which can handle different commit points for different contributors.

-------------------------------------------------------------------------------------------

III. How does this impact your graph?

Solution: 

a.The graph almost changes its shape. As most of the parameters (like height and width) are hardcoded, 
the magnitude of multiple nodes of the above repositories are not able to fit in the allocated space of the graph.
Maybe the further modifications to the graph are required to fit in the nodes in the allocated space.

b. With more data, say with 100 commits, the page load time becomes almost unresponsive for some time because of the 
time taken to load the large amount of data.

c. The graph becomes very messy without graphical interaction in it as it becomes difficult to trace the parent.

d. As we bring only 30 commits or 100 commits for each page, the overall picture for the whole repository cannot be determined and their 
may not be linkage between all the commit nodes.

-------------------------------------------------------------------------------------------

IV. How would you improve your visualization to address issues with the larger and more complex data?

Solution: 
i. The multiple commits done by the contributors at the same time needs to be focused and have to be placed at proper distance
so as to have a visual impact on the viewers. Maybe the multiple commit points can be grouped by each user and can be arranged and displayed in the form of single circle.
When that circle is hovered the multiple commit points with commit id (i.e. sha) and their timestamp can be shown.

ii. Interaction techniques needs to added. 
Only a set i.e. filtering of data should be only used from the whole repository, say : the commits from the last year can be fetched for the graph.






