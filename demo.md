```mermaid
graph TD
subgraph node
A[[Client]] --> B(["Cluster IP<br >(IP tables)"]) --> C{Kube-proxy}
style A fill:#B0C4DE, stroke: #B0C4DE
style B fill:#D3D3D3, stroke: #D3D3D3
style C fill: #FFE4E1, stroke:#FA8072
end
D{{API Server}} --> C{Kube-proxy}
style D fill:#98FB98, stroke: #3CB371
C{Kube-proxy} --> E["Backend Pod 1<br >labels: app = MyApp<br >Port: 9376"]
C{Kube-proxy} --> F["Backend Pod 2<br >labels: app = MyApp<br >Port: 9376"]
C{Kube-proxy} --> G["Backend Pod 3<br >labels: app = MyApp<br >Port: 9376"]
 ```