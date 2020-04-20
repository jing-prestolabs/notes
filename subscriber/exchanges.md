

## Upbit

telsocket -url wss://api.upbit.com/websocket/v1

[{"ticket":"UNIQUE\_TICKET"},{"type":"orderbook","codes":["BTC-ETH"]}]

[{"ticket":"UNIQUE\_TICKET"},{"type":"trade","codes":["BTC-ETH"]}]

## Coinone

telsocket -url wss://wss.coinone.co.kr/wsco.kr/ws

{"event":"subscribe", "channel":"orderbook", "trading\_pair":"BTC-KRW", "unit":"1000"}

{"event":"subscribe", "channel":"trades", "trading\_pairs":["ETH-KRW"]}

## Bithumb

telsocket -url pubwss.bithumb.com/pub/ws

{"type":"transaction", "symbols":["BTC\_KRW"]}

{"type":"orderbookdepth", "symbols":["BTC\_KRW"]}

## Liquid (For private api auth required)

telsocket -url wss://tap.liquid.com/app/LiquidTapClient?rate\_limit=15kbb

{"event":"pusher:subscribe", "data":{"channel":"price\_ladders\_cash\_btcjpy\_buy"}} 

{"event":"pusher:subscribe", "data":{"channel":"executions\_cash\_btcjpy"}}


