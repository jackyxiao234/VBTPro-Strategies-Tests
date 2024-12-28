from vectorbtpro import * 
import numba as njit
import datetime
import yfinance as yf

end_date = datetime.datetime.now()
start_date = datetime.datetime(2021, 1, 1)

data = vbt.YFData.pull(
    ['NVDA', 'AAPL'],
    start = start_date,
    end = end_date,
    missing_index = 'drop'  
)

print(aapl_price['Close'])

# multi_pf = vbt.Portfolio.from_holding(close = data)
