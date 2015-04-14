# 实验三：虚拟内存管理
做完实验二后，大家可以了解并掌握物理内存管理中的连续空间分配算法的具体实现以及如何建立二级页表。本次实验是在实验二的基础上，借助于页表机制和实验一中涉及的中断异常处理机制，完成Page
Fault异常处理和FIFO页替换算法的实现。实验原理最大的区别是在设计了如何在磁盘上缓存内存页，从而能够支持虚存管理，提供一个比实际物理内存空间“更大”的虚拟内存空间给系统使用。
```dot
digraph g{
	node [shape = record,height=.1];
 	node0[label = "<f0> |<f1> G|<f2> "]; 
        
       node1[label = "<f0> |<f1> E|<f2> "];
       node2[label = "<f0> |<f1> B|<f2> "]; 
       node3[label = "<f0> |<f1> F|<f2> "]; 
       node4[label = "<f0> |<f1> R|<f2> "]; 
       node5[label = "<f0> |<f1> H|<f2> "]; 
       node6[label = "<f0> |<f1> Y|<f2> "];
       node7[label = "<f0> |<f1> A|<f2> "];
       node8[label = "<f0> |<f1> C|<f2> "];
	
	"node0": f2->"node4":f1;
	"node0": f0->"node1":f1;
	"node1": f0->"node2":f1;
	"node1": f2->"node3":f1;
	"node2": f2->"node8":f1;
	"node2": f0->"node7":f1;
	"node4": f2->"node6":f1;
	"node4": f0->"node5":f1;
}
```

