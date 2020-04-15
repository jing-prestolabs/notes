./pyrunner coin/strategy/mm/tool/feed\_archive\_checker.py --trading\_date=20200218 --subsymbols=Bitmex:Futures:BTC-USD.PERPETUAL --worker\_ids=1,2 --feed\_machine=feed-05.ap-northeast-1.aws --use\_feed\_cache=True --time\_range=0-24 --feed\_cache\_dir=/home/leon/workspace/coin\_lm/coin/fastfeed\_out/feed-cache/ --api\_override=Futures:Bitmex=v1.realtime

bazel build -c dbg //cc/coin1/fastfeed:pyfastfeed.so
