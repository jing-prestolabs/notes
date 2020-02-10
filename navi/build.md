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
* ggooltest (release-1.6.0)
* clang (llvmorg-3.9.1)
* llvm (llvmorg-3.9.1)
### Dynamic Linking for EL8 Docker
* Setup envrionment: install bazel, change timezone, create '/data/log' dir.
* Remove protobuf-lite from third\-party/protobuf/BUILD
* Build Clang/LLVM static libs

## Statically Compile iosg apps
bazel build --config=opt //presto/feed\_subscriber/swordfish\_mds/swordfish\_mds_0\_15\_7\_4\_l2md:feed\_converter


bazel build --config=opt //presto/feed\_subscriber/swordfish\_mds/swordfish\_mds_0\_15\_7\_4\_l1md:feed\_converter


bazel build --config=opt //presto/feed\_subscriber/swordfish\_mds/swordfish\_mds_0\_15\_7\_4\_index:feed\_converter


bazel build --config=opt //presto/feed\_tool/feed\_interval:proto\_feed\_to\_price\_change\_feed

## Dynamically Compile iosg apps
bazel build --config=opt --config=dynamic\_linkg\_mode //presto/feed\_subscriber/swordfish\_mds/swordfish\_mds_0\_15\_7\_4\_l2md:feed\_converter


bazel build --config=opt --config=dynamic\_linkg\_mode //presto/feed\_subscriber/swordfish\_mds/swordfish\_mds_0\_15\_7\_4\_l1md:feed\_converter


bazel build --config=opt --config=dynamic\_linkg\_mode //presto/feed\_subscriber/swordfish\_mds/swordfish\_mds_0\_15\_7\_4\_index:feed\_converter


bazel build --config=opt --config=dynamic\_linkg\_mode //presto/feed\_tool/feed\_interval:proto\_feed\_to\_price\_change\_feed


