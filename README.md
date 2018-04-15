## 1、申请账号 
       url: `/api/applyAccount`
       method:`post`
###### 参数:
        {
              displayName:发送人显示名称，不是账号
              email:发送人的邮箱
              password:密码
        }
###### repuest:
      {"displayName":"yurx","email":"yurx001@qq.com","password":"yu001"}
###### reponse:
      {"code":200,"msg":"0x8ed140a532af2c45850aaa60b07f075795060a7c"} 
      
## 2、 获取用户积分
       url: `/api/getPoints?accountId=0xa8c4434e58e34df89e6fec62f7407ad2119f3f04`
       method:`get`
###### reponse:
      {"code":200,"msg":100000001}
   
## 3、转账功能 
       url: `/api/transfer`
       method:`post`
###### 参数:
        {
              fromAccount:发送人账号
              toAccount:接收人账号
              password:密码
              amount:金额
        }
###### repuest:
      {"fromAccount":"0xeb576b9bc32af424b90204f9e9eb4a6b13432363","toAccount":"0xa8c4434e58e34df89e6fec62f7407ad2119f3f04","password":"","amount":"20000"}
###### reponse:
      {"code":200,"msg":"transfer success,transaction hash:0x5c28f2749462e8f3d4ca8cb70153517c054f206176291a4adc4815bd132785d8"} 

## 4、获取所有用户信息
       url: `/api/getAccountList`
       method:`get`
###### 参数:
###### repuest:
###### reponse:
    {"code":200,"msg":["0xeb576b9bc32af424b90204f9e9eb4a6b13432363","0xa8c4434e58e34df89e6fec62f7407ad2119f3f04","0x8ed140a532af2c45850aaa60b07f075795060a7c","0x90cdb06f0a29f1296c97272371318a01b681aa98"]}
## 5、获取BlockList接口
       url: `/api/getBlockChainList`
       method:`post`
###### 参数:
###### repuest:
     {"page":1,"totalCount":1585,"pageSize":2}
###### reponse:
    {"code":200,"msg":{"list":[{"blockNumber":155563,"currentHash":"0xe7deea200fe945b976686908cef100a3574edfb7f8ca36f95d5d812091aec6d5","parentHash":"0xcf49f24eb58b4f2c66b328471a81e0fd2a69cc7a65e44f0bba1e616d485368e2","trasactionCount":0,"age":"1970-01-18 23:12:01.292"},{"blockNumber":155562,"currentHash":"0xcf49f24eb58b4f2c66b328471a81e0fd2a69cc7a65e44f0bba1e616d485368e2","parentHash":"0x821387ca0cc90cf3ffd28235c9c2d4c4ccee753664bce5db942a9ce2645d1dbe","trasactionCount":0,"age":"1970-01-18 23:12:01.291"}],"totalCount":155563,"page":1,"pageSize":2}}
## 6、获取区块明细
       url: `/api/getBlockDetail?blockId=158524`
       method:`get`
###### reponse:
      {"code":200,"msg":{"blockNumber":158524,"currentHash":"0xc541d52ec872a622f04493ed26b1fbb8642b2d8b25c82ac7659d2f7e5012f10d","parentHash":"0xde6600d3617b1aec393bf562c85c0f3c4c546b39c2705ffb3f46466c1061a6c8","age":1523338067,"transactionInfoList":[{"hash":"0xcc0be1c489e848170ada2888aeca64025514106a912f8c452bb00e3e0a3ff87e","amount":1,"from":"0xeb576b9bc32af424b90204f9e9eb4a6b13432363","to":"0xa8c4434e58e34df89e6fec62f7407ad2119f3f04","gas":90000,"gasPrice":1}]}}

## 7、登录
       url: `/api/login`
       method:`post`
###### repuest:
              {"account":"0xeb576b9bc32af424b90204f9e9eb4a6b13432363","password":""}
###### reponse:
     {"code":200,"msg":"success"}
     
## 8、获取目录菜单
       url: `/api/userMenu?accountId=0xa8c4434e58e34df89e6fec62f7407ad2119f3f01`
       method:`get`
###### reponse:
     {"code":200,"msg":[{"header":"BlockChain-BP","className":"fa-dashboard","items":[{"className":"fa-laptop","title":"管理","href":null,"children":[{"title":"查询积分","href":"/api/getPoints"},{"title":"积分转账","href":"/api/transfer"},{"title":"常用功能","href":"/api/getAccountList"},{"title":"区块列表","href":"/api/getBlockChainList"}]}]}]}
## 参数对照表 Eth  
---------------------------------------------------------------

    | no             | 字段                             | 说明    
    |---------------:|---------------------------------:|--------
    | 1              | blockNumber                      | 区块编号    
    | 2              | currentHash                      | 区块hash 
    | 3              | parentHash                       | 前一个区块hash
    | 4              | trasactionCount                  | 区块交易数量  
    | 5              | age                              | 区块产生时间 
    | 6              | hash                             | 交易记录hash 
    | 7              | amount                           | 积分 
    | 8              | from                             | 发送人 
    | 9              | to                               | 接收人
    | 10             | fromAccount                      | 发送人账号 
    | 11             | toAccount                        | 接收人账号 
    | 12             | password                         | 密码
    
    



 