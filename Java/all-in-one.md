# 热更新

1. classLoader
2. agent main, arthas
    1. `jad`命令，反编译；
    2. `mc`命令，编译；
    3. `redefine`命令，加载新的字节码；


# 异步流式接口

1. `ResponseBodyEmitter`;
2. `SseEmitter`;
3. `StreamingResponseBody`; 大文件下载

分布式场景下，重新连接的时候，会导致连接的节点不一样，无法重新获取到原来的`Emitter`，需要考虑引入分布式数据库，重新创建`Emitter`；
`Emitter`每次发送消息时，都需要从`Map`中重新获取，并处理前端断开连接的异常；