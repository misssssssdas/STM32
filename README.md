# STM32
STM32 CM3 Project
延时函数：

延时函数的初始化只用两行。
微秒级的延时使用SYSTICK的VAL，同时结合其心跳数大周期，使得该函数即使在延时过程被中断，最终的延时也会是准确的。
毫秒级的延时直接调用微秒延时函数，突破了原子函数延时不能超过2秒的限制。
另外，以72MHz工作频率实测值为基础，附带编写了软延时函数。

