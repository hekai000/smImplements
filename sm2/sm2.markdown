椭圆曲线

$y^2 = x^3 + ax + b$

其中，$a$ 和 $b$ 是椭圆曲线的参数，$a$ 和 $b$ 决定了椭圆曲线的形状。

计算：

椭圆曲线：$y^2 = x^3 + x + 1$

有限域：GF(23)

$y^2 = x^3 + x + 1$(mod 23)

$x_3 = k^2-x_1-x_2$(mod 23)
$y_3 = k(x_1-x_3) - y_1$(mod 23)

若P=Q，则$k=\frac{3x_1^2+a}{2y_1} (mod 23)$
若P≠Q，则$k=\frac{y_2-y_1}{x_2-x_1} (mod 23)$

P是基点，(0,1)
小数求模
负数求模 $x mod y = x - y * floor(x/y)$


Q=kP
消息为M，公钥为Q，私钥为k

加密：
C=(rP, M+rQ)

解密：
M=M+rQ-k(rP)=M+rQ-krP=M

SM2椭圆曲线：P256, $y^2=x^3-3x+b$
```
p=FFFFFFFEFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF00000000FFFFFFFFFFFFFFFF
a=FFFFFFFEFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF00000000FFFFFFFFFFFFFFFC
b=28E9FA9E9D9F5E344D5A9E4BCF6509A7F39789F515AB8F92DDBCBD414D940E93
n=FFFFFFFEFFFFFFFFFFFFFFFFFFFFFFFF7203DF6B21C6052B53BBF40939D54123
Gx=32C4AE2C1F1981195F9904466A39C9948FE30BBFF2660BE1715A4589334C74C7
Gy=BC3736A2F4F6779C59BDCEE36B692153D0A9877CC62A474002DF32E52139F0A0
```

SM2公钥加密过程：
![加密算法](加密算法过程.png)
![KDF密钥派生函数](KDF密钥派生函数.png)

SM2签名验签流程：
![数字签名](数字签名.png)
![验签](验签.png)


SM2密钥交换流程：
![alt text](密钥交换协议.png)