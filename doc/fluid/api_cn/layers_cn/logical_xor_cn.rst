.. _cn_api_fluid_layers_logical_xor:

logical_xor
-------------------------------

.. py:function:: paddle.fluid.layers.logical_xor(x, y, out=None, name=None)

logical_xor算子

它在 ``X`` 和 ``Y`` 上以元素方式操作，并返回 ``Out`` 。 ``X`` 、 ``Y`` 和 ``Out`` 是N维布尔张量（Tensor）。 ``Out`` 的每个元素的计算公式为：

.. math::
        Out = (X || Y) \&\& !(X \&\& Y)

参数：
        - **x** （Variable）- （LoDTensor）logical_xor算子的左操作数
        - **y** （Variable）- （LoDTensor）logical_xor算子的右操作数
        - **out** （Tensor）- 输出逻辑运算的张量。
        - **name** （basestring | None）- 输出的名称。

返回：        (LoDTensor)n维布尔张量。

返回类型：        输出（Variable）。



**代码示例：**

.. code-block:: python

    import paddle.fluid as fluid
    left = fluid.layers.data(
        name='left', shape=[1], dtype='bool')
    right = fluid.layers.data(
        name='right', shape=[1], dtype='bool')
    result = fluid.layers.logical_xor(x=left, y=right)






