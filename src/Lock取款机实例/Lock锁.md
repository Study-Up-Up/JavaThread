# Lock锁

## 1.定义

Synchronized原始采用的是CPU悲观锁机制，即线程获得的是独占锁。独占锁意味着其他线程只能依靠阻塞来等待线程释放锁。而在CPU转换线程阻塞时会引起线程上下文切换，当有很多线程竞争锁的时候，会引起CPU频繁的上下文切换导致效率很低。  
Lock用的是乐观锁方式。所谓乐观锁就是，每次不加锁而是假设没有冲突而去完成某项操作，如果因为冲突失败就重试，直到成功为止。

## 2.方法

lock.tryLock：尝试获取锁，否则等待获取

## 3.优势

Lock可以在两个方法中上锁和关锁，而Synchronized只能在一个方法中