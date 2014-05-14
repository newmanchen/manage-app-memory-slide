#Managing Your App's Memory
---
##How Android Manages Memory(cont')
+ Android does **NOT** offer swap space for memory
+ Using **[paging](http://en.wikipedia.org/wiki/Paging)** and **[memory-mapping](http://en.wikipedia.org/wiki/Memory-mapped_files)** instead
  + Only way to completely release memory from your app is to release object references you may be holding, making the memory available to the garbage collector. 
---
##How Android Manages Memory(cont')
+ Sharing Memory
+ Allocating and Reclaiming App Memory
+ Restricting App Memory
+ Switching Apps
---
##Sharing Memory
+ Most of the RAM pages allocated for framework code and resources to be shared across all app processes.
  + **Zygote** - starts when system boots and loads common framework code and resources
  + Each process is forked from Zygote
+ Most static data is mmapped into a process
  + Dalvik code (.odex file)
  + native code (.so file)
  + app resource
+ In many places, Android shares the same dynamic RAM across processes using explicitly allocated shared memory regions (either with ashmem or gralloc). For example, window surfaces use shared memory between the app and screen compositor, and cursor buffers use shared memory between the content provider and client.
---
##Allocating and Reclaiming App Memory

---
##Restricting App Memory

---
##Switching Apps

---
##How Your App Should Manage Memory
+ Use services sparingly
+ Release memory when your user interface becomes hidden
+ Release memory as memory becomes tight
+ Check how much memory you should use
+ Avoid wasting memory with bitmaps
+ se optimized data containers
+ Be aware of memory overhead
+ Be careful with code abstractions
+ Use nano protobufs for serialized data
+ Avoid dependency injection frameworks
+ Be careful about using external libraries
+ Optimize overall performance
+ Use ProGuard to strip out any unneeded code
+ Use zipalign on your final APK
+ Analyze your RAM usage
+ Use multiple processes