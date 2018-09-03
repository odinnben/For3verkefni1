  **1.Hvað er null og undfeind**
  
  null og undefined eru báðar data type javascript er með 7 basic data types og þau eru eitt af þeim 
  null er data type sem er með ekkert í sér alveg tómt en svo er 
  undefeind það getur verið með value í sér en ef þú ert ekki bæuinn að gefa henni value þá færð þú undefeind
  
  **2.Hvað gerir 'use strict' í JavaScript kóða?**
    
    use strict er mode sem er hjálpar þér að debugga kóðan þinn og 
    að notandi sem er að skrifa kóðan má ekki runa neima ef kóðinn er alveg 100% réttur
    
  **3.Hver er munurinn á let og var?**
  
  munnurin á þeim er í scopinum hjá þeim var er scopaður hjá nálægsta fuction blcok 
  let er nálægst enclosing block 
  en þau eru bæði global er þau er ekki inn í block
  
  **4.Skilgreindu fall á þrjá mismunandi vegu með kóðasýnidæmi.**
```javascript
    function eitthvað(1,2){
    let eitthvað = 1+2;
    return eitthvað
   }

  let eitthvað = function(1,2){
    let eitthvað = 1+2;
    return eitthvað
  };

  var eitthvað = x => x * x;
 ```
   __5.Útskýrðu hvað eftirfarandi kóði gerir, hvað gera svigarnir?__
  ```javascript
  (function() { alert('Hello World'); })();
  ```
  það sem kóðinn geiri er að seigja hello world á núverandi síðuno sem þú ert á það er sem alert gerir 
  það sem sviginn sem er fyrir framan fuction gerir það á privite fall svo sem er 
  fyrir bakið fuction lætur svo að þú getur bætt eitthvað inn í fuction
  sviginair eru lokaðir svo að kóðinn getur keyrt um leið og það er kveikt á honum 
  
   __6.Í hvaða röð er kóðinn keyrður í raun eftir að JS þýðandinn (e. interpreter) er búinn að fá hann til sín? Raðaðu kóðanum rétt fyrir JS þýðandanum.Afhverju er útkoman8? Útskýrðu.__
  

    function foo(){ 
      function bar() { 
        return 3; 
      } 
      return bar(); 
        function bar() { 
          return 8; 
        } 
      } 
      alert(foo()); 


þessi kóði keyir fyrstu línuna og svo seinni útkoman veður 8 út af því að fuction heitir það sama 
fuction sem er fyrir neðan overwritear hitt og þá veður útkoman 8 
      

kóðinn fyrir þýðenda
      
          function foo(){
          function bar() {
              return 3;
           }
           function bar() {
              return 8;
           }
            return bar();
          }
      alert(foo());

 
   **7.hver er munnurinn á for,for-in og for-off**
  
 for-off loppar yfir value
 for-inn loppar yfir nafni

   **8.forEach() Leystu  lið 20 í Arrays á Udacity https://classroom.udacity.com/courses/ud803**

```javascript
var test = [12, 929, 11, 3, 199, 1000, 7, 1, 24, 37, 4,
 19, 300, 3775, 299, 36, 209, 148, 169, 299,
 6, 109, 20, 58, 139, 59, 3, 1, 139
 ];

test.forEach(function (value, i, arr) {
    if (value % 3 === 0) {
        arr[i] += 100;
    }
});
```
  **9.Hvað gerir .map() fylkjaaðferðin? Leystu lið 22 í Arrays á Udacity https://classroom.udacity.com/courses/ud803**
```javascript
var bills = [50.23, 19.12, 34.01,
    100.11, 12.15, 9.90, 29.11, 12.99,
    10.00, 99.22, 102.20, 100.10, 6.77, 2.22
];

var totals = bills.map(function(bill) {
    bill += (bill * 0.15);
    
    return parseFloat(bill.toFixed(2));
})

console.log(totals)
```
  **10.Leystu lið 25 í Arrays í lesson 6á Udacity https://classroom.udacity.com/courses/ud803**
```javascript
var numbers = [
    [243, 12, 23, 12, 45, 45, 78, 66, 223, 3],
    [34, 2, 1, 553, 23, 4, 66, 23, 4, 55],
    [67, 56, 45, 553, 44, 55, 5, 428, 452, 3],
    [12, 31, 55, 445, 79, 44, 674, 224, 4, 21],
    [4, 2, 3, 52, 13, 51, 44, 1, 67, 5],
    [5, 65, 4, 5, 5, 6, 5, 43, 23, 4424],
    [74, 532, 6, 7, 35, 17, 89, 43, 43, 66],
    [53, 6, 89, 10, 23, 52, 111, 44, 109, 80],
    [67, 6, 53, 537, 2, 168, 16, 2, 1, 8],
    [76, 7, 9, 6, 3, 73, 77, 100, 56, 100]
];

for (var x = 0; x < numbers.length; x++) {
    for (var y = 0; y < numbers[x]. length; y++) {
        
        if (numbers[x][y] % 2 === 0) {
            numbers[x][y] = 'even';
        } else {
            numbers[x][y] = 'odd';
        }
        
    }
}
console.log(numbers);
```
