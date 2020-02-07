## Compile Navi
### Static
bazel build -k //...
### Dynamic 
bazel build -k //... --config dynamic\_linking\_mode
### Static EL8
Need to manually build the following static libs:
* protobuf (v3.3.0)
* gflags (v2.2.1)
* glog (v0.3.5)
* clang (llvmorg-3.9.1)
* llvm (llvmorg-3.9.1)

## Compile iosg apps
bazel build --config=opt //presto/feed\_subscriber/swordfish\_mds/swordfish\_mds_0\_15\_7\_4\_l2md:feed\_converter
bazel build --config=opt //presto/feed\_tool/feed\_interval/proto\_feed\_to\_price\_change\_feed
