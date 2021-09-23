```
function highAndLow(numbers){
 
  numbers = numbers.split(' ');
  let bigNum = numbers[0];
  let smallNum = numbers[0];
  
  for( let i = 0; i < numbers.length; i++ ) {
    
    if(+numbers[i] > +bigNum) {
      bigNum = numbers[i];
    }
    if(+numbers[i] < +smallNum) {
      smallNum = numbers[i];
    }
  }
  return `${bigNum} ${smallNum}`;
}
console.log(highAndLow("8 3 -5 42 -1 0 0 -9 4 7 4 -4"));
```
```
const chai = require("chai");
const assert = chai.assert;
chai.config.truncateThreshold=0;

describe("Basic tests", () => {
  it("Testing for fixed tests", () => {
    assert.strictEqual(highAndLow("8 3 -5 42 -1 0 0 -9 4 7 4 -4"), "42 -9");   
  });
});
```
**You have passed all of the tests! :)**
