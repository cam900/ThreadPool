ThreadPool
==========

A simple C++11 Thread Pool implementation.
Thread Pool wait function added by cam900

Basic usage:
```c++
// create thread pool with 4 worker threads
ThreadPool pool(4);

// enqueue and store future
auto result = pool.enqueue([](int answer) { return answer; }, 42);

// wait until all tasks in thread pool are done
pool.wait_for_tasks();

// get result from future
std::cout << result.get() << std::endl;

```
