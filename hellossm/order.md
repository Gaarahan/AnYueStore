订单测试用例:
    获取用户所有订单:
       get访问(带token) http://47.94.108.73:8080/ayms/order/showOrder
       返回值见图
       
   获取所有订单之后点击某一订单详情时,访问
    http://47.94.108.73:8080/ayms/order/showOneOrder?orderId=xx
         xx为接收的id
         返回:见图
        
        
   用户点击取消订单时,访问接口
    http://47.94.108.73:8080/ayms/order/cancelOrder?order=xx  --> xx为当前要取消订单的订单号
         
    
   点击下单时,添加订单:
    http://47.94.108.73:8080/ayms/order/createOrder
    前端
     {
       	"addrId":3,
       	"itemList":[
       		{
       			"commId":3,
       			"commSize":"XL",
       			"commColor":"haha",
       			"itemNum":5,
       			"itemPrice":19999
       		},
       		{
       			"commId":4,
       			"commSize":"XL",
       			"commColor":"aha",
       			"itemNum":41,
       			"itemPrice":19991
       		}
       		]
     }
    返回: 
    
     {
         "orderId": 14,
         "status": 200
     }
     orderId为新添加的订单id,在接收到id后传入订单详情页,请求:
     http://47.94.108.73:8080/ayms/order/showOneOrder?orderId=xx
     xx为接收的id
