# Creation of priority Queue
It creates a max-heap.
```
priority_queue<int> pq;
priority_queue<int, vector<int>, CmpClass> pq;
```

CmpClass is a custom comparator class for defining the order in priority queue.
By default, it is lesser\<T> ,you can change it to greater\<T>. In priority_queue , the ordering is inverse of comparator, meaning lesser<T> will order the keys in increasing values, but in priority_queue it will end in opposite i.e. in decreasing order.


## Custom CompareClass
```
priority_queue<pair<int,int>, vector<pair<int,int>>, CmpClass> pq;

	struct CmpClass {
		constexpr bool operator()(const pair<int,int>& a,const pair<int,int>& b){
		return a.second>b.second;
	}
};
```

