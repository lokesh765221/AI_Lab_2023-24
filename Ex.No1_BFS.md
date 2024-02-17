graph={
    '2':['3','4'],
    '3':['5'],
    '4':['6','7'],
    '6':[ ],
    '5':['6'],
    '7':['8'],
    '8':[ ]
}
visited=[]
queue=[]
def bfs(visted,node,graph):
    visited.append(node)
    queue.append(node)
    while queue:
        m=queue.pop(0)
        print(m)
        for neighbour in graph[m]:
            if neighbour not in visited:
                visited.append(neighbour)
                queue.append(neighbour)
print("BFS order is")
bfs(visited,'2',graph)
