```
function disemvowel(str) {
  str = str.replace(/[euioa]/gi, '');
  return str;
}
console.log(disemvowel("This website is for losers LOL!"));
console.log(disemvowel("No offense but,\nYour writing is among the worst I've ever read"));
console.log(disemvowel("What are you, a communist?"));
```
```
const { assert } = require("chai")

describe("Basic tests", () => {
  it("Testing for fixed tests", () => {
    assert.strictEqual(disemvowel("This website is for losers LOL!"), "Ths wbst s fr lsrs LL!")
    assert.strictEqual(disemvowel("No offense but,\nYour writing is among the worst I've ever read"), "N ffns bt,\nYr wrtng s mng th wrst 'v vr rd")
    assert.strictEqual(disemvowel("What are you, a communist?"), "Wht r y,  cmmnst?")
    })
  })
```
**You have passed all of the tests! :)**
