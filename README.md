
使用指南1.1.x:https://github.com/changmingxie/tcc-transaction/wiki/%E4%BD%BF%E7%94%A8%E6%8C%87%E5%8D%971.1.x

1.1.x 源码分支：https://github.com/changmingxie/tcc-transaction/tree/master

使用指南1.2.x:https://github.com/changmingxie/tcc-transaction/wiki/%E4%BD%BF%E7%94%A8%E6%8C%87%E5%8D%971.2.x

1.2.x 源码分支：https://github.com/changmingxie/tcc-transaction/tree/master-1.2.x

1.2.x 版本不向下兼容1.1.x，主要在声明tcc服务方法的注解有改变。1.2.x不同于1.1.x主要的地方在于发布服务时不再强制要求服务方法参数必须有TransactionContext参数，从而减少对业务代码的侵入。



Try: 尝试执行业务

    完成所有业务检查（一致性）

    预留必须业务资源（准隔离性）

Confirm: 确认执行业务

    真正执行业务

    不作任何业务检查

    只使用Try阶段预留的业务资源

    Confirm操作满足幂等性

Cancel: 取消执行业务

    释放Try阶段预留的业务资源

    Cancel操作满足幂等性

