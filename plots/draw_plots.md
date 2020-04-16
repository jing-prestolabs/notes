./pyrunner coin/strategy/mm/tool/feed\_archive\_checker.py --trading\_date=20200416 --subsymbols=Bithumb:Spot:BTC-USD --worker\_ids=1,2 --feed\_machine=test-machine --use\_feed\_cache=True --time\_range=0-24 --feed\_cache\_dir=/home/jing/data/fastfeed/ --api\_override=Spot:Bithumb=v2.realtime

bazel build -c dbg //cc/coin1/fastfeed:pyfastfeed.so
