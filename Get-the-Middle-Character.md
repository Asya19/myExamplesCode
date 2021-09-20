```   
function getMiddle(s)
{
  if(s.length === 0)
    return underfind;
  if(s.length === 1)
    return s[0];
  
  const middle = s.length / 2;
  
  if(s.length % 2 == 1) {
    let oddMid = s[Math.floor(middle)];
    return oddMid;
  }
  else {
    let honestMid = s[middle - 1] + s[middle];
    return honestMid;
  }
  console.log(getMiddle(s));
}  
```
```
describe("GetMiddle", function() {
  it("Tests", function() {
    Test.assertEquals(getMiddle("test"),"es");
    Test.assertEquals(getMiddle("testing"),"t");
    Test.assertEquals(getMiddle("middle"),"dd");
    Test.assertEquals(getMiddle("A"),"A");
  });
});
```
**You have passed all of the tests! :)**
