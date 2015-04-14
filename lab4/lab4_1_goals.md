
## 1. 实验目的

* 了解内核线程创建/执行的管理过程
* 了解内核线程的切换和基本调度过程
```dot
digraph g {

	overlap=false;
	rankdir = BT;
	node [shape=record];
	subgraph Atlantis {
		Tour;
		Order;
		CollectionPoint;
		TakePointTourist;
		TransportOwner;
		BusItem;
		ReturnPointTourist;

		Tour -> Order[label="" len=4.00];
		Order -> Tour[label="" len=4.00];
		CollectionPoint -> TakePointTourist[label="" len=4.00];
		TransportOwner -> BusItem[label="" len=4.00];
		CollectionPoint -> ReturnPointTourist[label="" len=4.00];
	}
}
```
```dot
digraph g {

	overlap=false;
	rankdir = BT;
	node [shape=record];
	subgraph Atlantis {
		Tour;
		Order;
		CollectionPoint;
		TakePointTourist;
		TransportOwner;
		BusItem;
		ReturnPointTourist;

		Tour -> Order[label="" len=4.00];
		Order -> Tour[label="" len=4.00];
		CollectionPoint -> TakePointTourist[label="" len=4.00];
		TransportOwner -> BusItem[label="" len=4.00];
		CollectionPoint -> ReturnPointTourist[label="" len=4.00];
	}
}
```
```dot
digraph g {

	overlap=false;
	rankdir = BT;
	node [shape=record];
	subgraph Atlantis {
		Tour;
		Order;
		CollectionPoint;
		TakePointTourist;
		TransportOwner;
		BusItem;
		ReturnPointTourist;

		Tour -> Order[label="" len=4.00];
		Order -> Tour[label="" len=4.00];
		CollectionPoint -> TakePointTourist[label="" len=4.00];
		TransportOwner -> BusItem[label="" len=4.00];
		CollectionPoint -> ReturnPointTourist[label="" len=4.00];
	}
}
```
