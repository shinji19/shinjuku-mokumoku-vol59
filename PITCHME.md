### 技術書展に向けての準備



---


### ccxt技術検証

```python
import time
import sys
import ccxt

# ccxt sample
# https://github.com/ccxt/ccxt/blob/master/examples/py/tickers.py

# TODO あとで引数の対応
# id = sys.argv[1]
# exchange = getattr(ccxt, id)()
exchange = ccxt.bitflyer()
markets = exchange.load_markets()
# load_marketsで発生するエラー　要調査
'''
except ccxt.DDoSProtection as e:
    dump(yellow(type(e).__name__), e.args)
except ccxt.RequestTimeout as e:
    dump(yellow(type(e).__name__), e.args)
except ccxt.AuthenticationError as e:
    dump(yellow(type(e).__name__), e.args)
except ccxt.ExchangeNotAvailable as e:
    dump(yellow(type(e).__name__), e.args)
except ccxt.ExchangeError as e:
    dump(yellow(type(e).__name__), e.args)
except ccxt.NetworkError as e:
    dump(yellow(type(e).__name__), e.args)
except Exception as e:  # reraise all other exceptions
    raise
'''
```

---


### 3枚目のスライド


---


### おわり
