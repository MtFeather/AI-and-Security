# 建立線性迴歸分析模型:用氣溫來預測冰紅茶的銷售量
- 使用 sklearn.linear_model 的 LinearRegression() 方法
```python
import numpy as np
from sklearn.linear_model import LinearRegression

# 資料==> 使用np.array來建立氣溫及冰紅茶的銷售量
temperatures = np.array([29, 28, 34, 31, 25, 29, 32, 31, 24, 33, 25, 31, 26, 30])
iced_tea_sales = np.array([77, 62, 93, 84, 59, 64, 80, 75, 58, 91, 51, 73, 65, 84])

# 先建立線性迴歸的物件
lm = LinearRegression()

# 再用線性迴歸物件的fit()函式進行分析
lm.fit(np.reshape(temperatures, (len(temperatures), 1)), np.reshape(iced_tea_sales, (len(iced_tea_sales), 1)))


# 印出係數
print(lm.coef_)

# 印出截距
print(lm.intercept_ )
```
