# Google Colaboratory
Colaboratory 是免費的 Jupyter 筆記本環境，不需要進行任何設置就可以使用，並且完全在雲端運行。要了解更多信息，請參閱我們的[常見問題解答](https://colab.research.google.com/notebooks/basic_features_overview.ipynb)。

## 完成矩陣相乘
建立矩陣相乘的程式碼，完成後點擊左邊執行程式，第一次因為tensorflow須建立模型，所以會等一段時間。
![googlecola](/images/googlecola01.PNG)


# 在Google Colab安裝PyTorch
Torch 自稱為神經網絡界的Numpy, 因為他能將torch 產生的tensor 放在GPU 中加速運算(前提是你有合適的GPU), 就像Numpy 會把array 放在CPU 中加速運算. 所以神經網絡的話, 當然是用Torch 的tensor 形式數據最好咯. 就像Tensorflow 當中的tensor 一樣。

## 修改Colaboratory的環境配置
將硬體環境改為使用GPU，修改 > 記事本設置 > 硬體加速器 > GPU
![colab01](/images/colab01.png)
![colab02](/images/colab02.PNG)

## 開始安裝
- 首先在Google Colaboratory安裝Torch
```python
!pip3 install http://download.pytorch.org/whl/cu80/torch-0.4.1-cp36-cp36m-linux_x86_64.whl
```
![colab03](/images/colab03.PNG)

- 在安裝torchvision，此是服務於pytorch深度學習框架的, 用來生成圖片視頻數據集, 和一些流行的模型類和預訓練模型。
```python
!pip3 install torchvision
```
![colab04](/images/colab04.PNG)

## 驗證
- 為確保正確安裝PyTorch，我們可以通過運行示例PyTorch代碼來驗證安裝。在這裡，我們將構造一個隨機初始化的張量。
```python
from __future__ import print_function
import torch
x = torch.rand(5, 3)
print(x)
```
![colab05](/images/colab05.PNG)

- 此外，要檢查PyTorch是否啟用並可訪問您的GPU驅動程序和CUDA，請運行以下命令以返回是否啟用了CUDA驅動程序：
```python
import torch
torch.cuda.is_available()
```
![colab06](/images/colab06.PNG)



