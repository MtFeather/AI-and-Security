# Getting started with TensorFlow
> Getting started with TensorFlow
>
> <<深度學習快速入門：使用TensorFlow>> 
>
> 作者： Giancarlo Zaccone  譯者： 傅運文  
>
> 出版社：博碩  出版日期：2017/01/11 
>
> https://github.com/PacktPublishing/Getting-Started-with-TensorFlow

## 執行第一支程式 "Chapter 1/first_session_only_tensorflow.py"
```python
#first_session_only_tensorflow.py

import tensorflow as tf

x = tf.constant(1, name='x')
y = tf.Variable(x+9,name='y')


model = tf.initialize_all_variables()

with tf.Session() as session:
    session.run(model)
print(session.run(y))
```
