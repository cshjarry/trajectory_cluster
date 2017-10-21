# trajectory_cluster
# A Simple cluster Algorithm 
对任意两条路径计算相似度，具体来说，当计算
   $$ Similarity_{r_{1}->r_{2}} = \frac{N(p)}{N(r_{1})} $$
   $N(p)$为r1中靠近r2的点的个数,$N(r1)$为r1的路径点的总个数，$ Similarity_{r_{1}->r_{2}}$就是$ r_{1}$对$r_{2} $的相似度，或者说两者之间的距离
   
而检查$r1$中某个p点是否靠近一条路径$r_2$，若这条路径$r_2$中
    $$\exists x \in r_2, distance(x, p) <= \varepsilon_1$$
$ \varepsilon_1 $为一个阈值,表示两个点是否邻近,$distance(x, p)$为两点之间的欧氏距离

若对$r_1$和$r_2$来说，满足
$$ Similarity_{r_{1}->r_{2}} >= \varepsilon_2 \ and \  Similarity_{r_{2}->r_{1}} >= \varepsilon_2$$
则可以判定两条路径属于同一个簇
      
