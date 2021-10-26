## exercise1

1. Distance:  numpy.linalg.norm(x, ord): ord=1,2,inf(max)
2. How to find k smallest/biggest values(or the index) in a list: 
  * np.partition(x,k)[:k]   
    > select k smallest values
  * np.argpartition(x,k)[:k]   
    > select k smallest values of index
  * np.partition(x,-k)[-k:]   
    > select k biggest values
  * np.argpartition(x,-k)[-k:]   
    > select k biggest values of index
3. obtain the frequency of each element provided inside a numpy array:
  - np.bincount([1, 2, 3, 4, 5, 1, 2, 1, 1, 1]) -> [0, 5, 2, 1, 1, 1],  
    > 0出现0次, 1出现5次...
  - np.bincount([1, 2, 3, 4, 5, 1, 2, 1, 1, 1]).argmax() -> 1, 
    > 就能找出谁出现最多是1
  - np.bincount([1, 1, 2, 2, 3, 3]).argmax() -> 1
    > 出现同样多次选最小的
4. label accuracy
  - test and pred are n-d array, accuracy = np.where(test-pred==0, 1, 0).sum()/test.shape[0]
    > broadcast **np.where(condition, ifyesthen, elsethen)**
  
