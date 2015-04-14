# 实验五：用户进程管理
```dot
digraph g {
	subgraph cluster0 {
		node[style = filled, color = white];

		style = filled;

		color = lightgrey;

		a0->a1->a2->a3;
		label = "prcess #1";
	}

	subgraph cluster1 {
		node[style = filled];
		b0->b1->b2->b3;
		label = "process #2";
		color = blue;
	}

	start->a0;
	start->b0;
	a1->b3;
	b2->a3;
	a3->end;
	b3->end;
	
	start[shape=Mdiamond];
	end[shape=Msquare];
}
```