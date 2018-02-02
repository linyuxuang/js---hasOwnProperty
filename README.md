# js---hasOwnProperty
hasOwnProperty作用



        hasOwnProperty：是用来判断一个对象是否有你给出名称的属性或对象。
        不过需要注意的是，此方法无法检查该对象的原型链中是否具有该属性，
        该属性必须是对象本身的一个成员。格式如下： 
      
       Js代码 

         1. object.hasOwnProperty(proName);  

         object.hasOwnProperty(proName); 

         判断proName的名称是不是object对象的一个属性或对象。 

     
         举例如下： 
          Js代码 
        
          得到false， 因为不能检测原型链中的属性
       1. var bStr = "Test String".hasOwnProperty("split");   

          String对象的原型上本来就有这个属性,自然返回true  
       2. var bStr1 = String.prototype.hasOwnProperty("split"); 

         返回true，因为不是检测原型中的属性  
       3. var bObj = ({fnTest:function(){}}).hasOwnProperty("fnTest"); 



    Object 对象 

      Object 对象自身用处不大，不过在了解其他类之前，还是应该了解它。
      因为 ECMAScript 中的 Object 对象与 Java 中的 java.lang.object 相似，
      ECMAScript 中的所有对象都由这个对象继承而来，Object 对象中的所有属性和方法都会出现在其他对象中，
      所以理解了 Object 对象，就可以更好地理解其他对象。 
      
      Object 对象具有下列属性： 

      constructor 
          对创建对象的函数的引用（指针）。对于 Object 对象，该指针指向原始的 Object() 函数。 
          
      Prototype 
          对该对象的对象原型的引用。对于所有的对象，它默认返回 Object 对象的一个实例。 
          

      Object 对象还具有几个方法： 

      hasOwnProperty(property) 
          判断对象是否有某个特定的属性。必须用字符串指定该属性。（例如，o.hasOwnProperty("name")） 
          
      IsPrototypeOf(object) 
          判断该对象是否为另一个对象的原型。 
          
      PropertyIsEnumerable 
          判断给定的属性是否可以用 for...in 语句进行枚举。 
          
      ToString() 
          返回对象的原始字符串表示。对于 Object 对象，ECMA-262 没有定义这个值，
          所以不同的 ECMAScript 实现具有不同的值。 
          
      ValueOf() 
          返回最适合该对象的原始值。对于许多对象，该方法返回的值都与 ToString() 的返回值相同。



















