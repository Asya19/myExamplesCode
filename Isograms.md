```
function isIsogram(str) {

   let i, j
   str = str.toLowerCase();
  
  for(i = 0; i < str.length; ++i) {
      for(j = i + 1; j < str.length; ++j)  {
          if( str[i] === str[j]){
            return false;
          }
      }
  }
  return true;
  
}

console.log(isIsogram("Dermatoglyphics"));
console.log(isIsogram("isogram"));
console.log(isIsogram("aba"));
console.log(isIsogram("moOse"));
console.log(isIsogram("isIsogram"));
console.log(isIsogram(""));
  ```          
  
