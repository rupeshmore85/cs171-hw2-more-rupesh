Questions:
 
I.
For each of the 5 visualizations listed above plus the calendar map, answer the following questions:
 
1. Who is the audience? (e.g. project manager, contributor, project user, visitor, etc.)
 
I think the audience is everyone interested in the repository:
 
Project Manager: He/She managing the repository can view the Contributors page and can find the number of members contributed to the repository. The Visualization graphs can be used for presentation to others.
Historical activities can be fetched for additional analysis. With punchcard the weekly activity can be studied with the time scale(At what time of the week most of the members commit the data etc)
 
Contributor: The Contributor to the repository can also view the contributions he/she or other contributors have made. The contributions he/she or others have made to the repository can also be tracked. The person can check the commit activity done and follow up with the commit and probably review and provide comments if any discrepancies. Commit activity for the past one year with a week by week breakdown can be seen. Pulse can be useful for viewing the historical activity. The other contributors profile and contributions can be seen on his public contributions graph.
 
Project User: A user following the project can keep a track of the repository. New functionality added to the project can be used or tested. The visualizations can be helpful to project user as he can study or work with the contributors to the repository.
 
Visitor: A visitor visiting can get a very good view of the repository by viewing all the visualizations. Pulse is a great way to discover recent activity on projects for visitors. Pulse will show you who has been actively committing and what has changed in a project's default branch. New and merged pull requests, open and closed issues, and unresolved discussions can also be viewed with ease.
 
 
 
2. What data have been used? How can you get the data using the GitHub API? (Note that it can be the combination of multiple queries and their processing).
 
Commit activity, contributors, code frequency (# of additions and deletions),
 
For the Caleydo/caleydo repository: https://github.com/Caleydo/caleydo
 
1. Commit data:
 
a. 30 commits
https://api.github.com/repos/caleydo/caleydo/commits
 
b. Page: 1 Commits: 100
https://api.github.com/repos/caleydo/caleydo/commits?page=1&per_page=100
 
2. Contributors:
 
https://api.github.com/repos/caleydo/caleydo/contributors
 
3. Code Frequency:
 
https://api.github.com/repos/caleydo/caleydo/stats/code_frequency
 
4. Punch Card:
 
https://api.github.com/repos/caleydo/caleydo/stats/punch_card
 
5. Pulse:
 
The data retrieved with the above 4 repositories can help in gathering information for pulse.
 
 
 
 
3. Those visualizations are updated over time. What happens if suddenly a contributor pushes many commits in a short time interval? How would you address this particular issue?
 
Many commits can be pushed at the same time. To manage those in graphs the nodes associated with each commit and for displaying in the graph we need to properly divide the time scale so that even commits within microseconds time difference can be properly displayed on the time scale and then can be properly linked to its parent branches.
 
 
II.
GitHub Network Graph:
 
 
1. What is the role of interaction for this visualization? Would a static graph have been sufficient?

Interaction is important for this visualization in the sense that with each new commit to the repository, the commit node should
appear in the Graph. So a static graph is not at all sufficient where a graph is dependent on the future commits by contributors.

 
 
2. What happens if many new developers suddenly join the project and push commits for the first time? 
How would you preserve the graph's readability in such a situation?

Since many developers commit at the same time, each developer will be assigned a different color. 
If more than one commit appear at the same time, i would display the node circle svg with a slightly bigger radius.
When someone hovers the mouse to the node, a popup will appear with all commit details in it. Obviously the popup size will also be
bigger which will fit the commit details.