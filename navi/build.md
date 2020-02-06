## Compile Navi
### Static
bazel build -k //...
### Dynamic 
bazel build -k //... --config dynamic\_linking\_mode

## Compile iosg apps
bazel build --config=opt //presto/feed\_subscriber/swordfish\_mds/swordfish\_mds_0\_15\_7\_4\_l2md:feed\_converter
