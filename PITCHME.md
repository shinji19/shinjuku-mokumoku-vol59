### 技術書展に向けての準備



---


### 技術検証

```dockerfile
FROM python:3.7.4

RUN pip install ccxt==1.18.1041 pylint==2.3.1 autopep8==1.4.4
```

```docker-compose
version: '3.7'
services:
  python:
    build: ./
    working_dir: /opt/ccxt-guidebook
    volumes:
      - ./:/opt/ccxt-guidebook
    command: tail -f /dev/null
```


### 技術検証

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


### 技術検証


---


### おわり
