# Managing Your App's Memory
---
## How Android Manages Memory

+Sharing Memory
+Allocating and Reclaiming App Memory
+Restricting App Memory
+Switching Apps

Note: This will only appear in the speaker notes window.
---
##How Your App Should Manage Memory
+Use services sparingly
+Release memory when your user interface becomes hidden
+Release memory as memory becomes tight
+Check how much memory you should use
+Avoid wasting memory with bitmaps
+se optimized data containers
+Be aware of memory overhead
+Be careful with code abstractions
+Use nano protobufs for serialized data
+Avoid dependency injection frameworks
+Be careful about using external libraries
+Optimize overall performance
+Use ProGuard to strip out any unneeded code
+Use zipalign on your final APK
+Analyze your RAM usage
+Use multiple processes