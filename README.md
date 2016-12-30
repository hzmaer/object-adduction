# object-adduction
对象引用

首先先答以下几个题目

(1)var a=3;

   b=a;
   
   var a=2;
   
   console.debug(a);//2
   
   console.debug(b);//3
   
   知识点：基本类型(字符串，数值，布尔值，underfined,null)的赋值。
   
(2)var a=3;

   b=a;
   
   var b=2;
   
   console.debug(a);//3
   
   console.debug(b);//2
   
   知识点：基本类型的赋值。
   
(3)var a=[1,2,3];

   var b=a;
   
   a.push(4);
   
   console.debug(a);//[1,2,3,4]
   
   console.debug(b);//[1,2,3,4]
   
   知识点：对象的引用
   
(4)var a=[1,2,3];

   var b=a;
   
   b.push(4);
   
   console.debug(a);//[1,2,3,4]
   
   console.debug(b);//[1,2,3,4]   
   
   知识点：对象的引用（a和b共用同一个地址，所以a和b中任何一个值改变了都会影响另外一个的值）
   
(5)var a=[1,2,3];
   
       b=a;
   
   var b=[1,2,3,4];
   
   console.debug(a);//[1,2,3]
   
   console.debug(b);//[1,2,3,4]
   
   知识点：var b=[1,2,3,4];这一行代码重新创建了一个变量b,跟之前的a,和b不在共用一个地址。所以不会影响a。
   
(6)var a=[1,2,3];
   
       b=a;
   
   var a=[1,2,3,4];
   
   console.debug(a);//[1,2,3,4]
   
   console.debug(b);//[1,2,3]   
   
   同5
   
(7)var obj={

       a:2
   
       };
   
   obj2=obj;
   
   obj.a=3;
   
   console.debug(obj.a);//3
   
   console.debug(obj2.a);//3
  
  知识点：obj和obj2公用同一个引用
  
(8)var obj={

       a:2
   
       };
   
   obj2=obj;
   
   obj2.a=3;
   
   console.debug(obj.a);//
   
   console.debug(obj2.a);//
   
  知识点：obj和obj2公用同一个引用。（这种改变一个对象的属性后另一个对象的属性也发生变化的引用方法会带来一些引用上的缺陷，下面再看看深拷贝和浅拷贝） 
  
(9)浅拷贝

  var obj={

      a:2
      
   }
   
   function copy(obj){
   
   var newObj={};
   
   for(var attr in obj){
   
   newObj[attr]=obj[attr];
   
   }
   
   return newObj;
   
   }
   obj2=copy(obj);
   
   obj2.a=3;
   
   console.debug(obj.a);  //2
   
   知识点：把对象的引用变为拷贝值（基本类型的赋值）
   
 (10)深拷贝

  var obj={

      a:{b:2}
   };
   
   function deepCopy(obj){
   
   if(typeof obj!= 'object'){
      
      return obj;
      
   };
   
   var newObj={};
   
   for(var attr in obj){
   
   newObj[attr]=deepCopy(obj[attr]);
   
   };
   
   return newObj;
   
   }
   obj2=deepCopy(obj);
   
   obj2.a.b=3;
   
   console.debug(obj.a.b);  //2
   
   }
   
   知识点：把对象的引用变为拷贝值（基本类型的赋值）
   
   

   
   
   
   
