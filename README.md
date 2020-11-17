#social-network-analysis
This project aims to investigate the mental health discussion taking part in UK health forum. We want to focus on bipolar forum available in https://www.mentalhealthforum.net/forum/threads/rollercoaster-ride-called-bipolar.198331/ The forum contains a large set of threads initiated by one member together with associated set of replies from other users.

From the forum, scrap the dataset utilizing only threads which contain more than 10 replies. You can either use the forum API, or through manual download in some structured database, which includes thread messages and their initiated user IDs, associated replies with their user IDs and time of posts.
Trace the plot showing the number of threads per user ID. Test whether the distribution of the number of threats per user follows Power-Law distribution or not. Justify your answer using appropriate statistical test.
Use a manual labelling of the threats indicating some keywords / topics in the discussion threat, and conclude how the topics of thread vary for the ten most active users.
Construct a network in the following way. The nodes correspond to the user IDs, while an edge between two nodes is established if the two users occur within the same thread (either in the reply section or as the thread initiator).
Summarize the attributes of the constructed graph in terms of Number of nodes, Number of edges, Overall clustering coefficient, average path length, size of giant component, diameter, maximum degree, average degree, number of communities using Girvan-Newman algorithm and the associated quality metrics as implemented in NetworkX.
We would like to take into account the number of replies initiated by the same user with the same threat, and whether the node has initiated a threat or is only involved in the replies of another threat. For this purpose, construct a weighted network in the following way. An edge between node A and node B is established with a maximum weight 10 if either A or B is the user ID who initiated the threat, otherwise, if both A and B occur as replies in the same threat, then the weight of edge A-B is equal to the total number of replies issued by A and B.
Repeat question 3) when using the newly established network.
Compare the nodes that achieve the highest score of centrality value, in-betweeness centrality and closeness centrality in both network of question 1) and that of question 4).
Now we would like to take into account the available timing information of the post. For this purpose, we would like to construct another network from the original network in question 1. For this purpose, we would like to elaborate a new weighted graph such that the weights take into account the timing information. More specifically, we would like to edge between node A and node B is weighted according to time response taken by A and B to respond to the last message. Design and implement a script that allows you to construct the new network.
Summarize the main the attributes of the constructed graph in terms of Number of nodes, Number of edges, Overall clustering coefficient, average path length, size of giant component, diameter.
Compare the most influential nodes in terms of centrality value, page-rank centrality, In- betweeness centrality and closeness centrality.
Discuss and comment, and use appropriate health literature in order to reinforce your interpretations.
