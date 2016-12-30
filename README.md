# object-adduction
对象引用

首先先答以下几个题目

(1)var a=3;

       b=a;
   
   var a=2;
   
   console.debug(a);//2
   
   console.debug(b);//3
   
(2)var a=3;

       b=a;
   
   var b=2;
   
   console.debug(a);//3
   
   console.debug(b);//2
   
(3)var a=[1,2,3];

       b=a;
   
       a.push(4);
   
   console.debug(a);//[1,2,3,4]
   
   console.debug(b);//[1,2,3,4]
   
(4)var a=[1,2,3];

       b=a;
   
       b.push(4);
   
   console.debug(a);//[1,2,3,4]
   
   console.debug(b);//[1,2,3,4]   

(5)var a=[1,2,3];
   
       b=a;
   
   var b=[1,2,3,4];
   
   console.debug(a);//[1,2,3]
   
   console.debug(b);//[1,2,3,4]
   
(6)var a=[1,2,3];
   
       b=a;
   
   var a=[1,2,3,4];
   
   console.debug(a);//[1,2,3,4]
   
   console.debug(b);//[1,2,3]   
   
(7)var obj={

       a:2;
   
       }
   
   obj2=obj;
   
   obj2.a=3;
   
   console.debug(obj.a);//
   
   console.debug(obj2.a);//
   
(8)var obj={

       a:2;
   
       }
   
   obj2=obj;
   
   obj2.a=3;
   
   alert(obj.a);   
   
(9)var obj={

      a:2;
      
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
   
   alert(obj.a);  
   
   

   
   
   
   
