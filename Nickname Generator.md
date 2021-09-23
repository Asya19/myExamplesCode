```
function nicknameGenerator(name) {
    let consonant = 'qwrtypsdfghjklzxcvbnm';
    consonant = consonant.split('');
    let vowel = 'euioa';
    vowel = vowel.split('');
  
    for (let i = 0; i < consonant.length; i++) {
      if(name.length <= 3) {
       return "Error: Name too short";
    }

        if (name[2] == consonant[i]) {
          
            return name.slice(0, 3);
        }

        if (name[2] == vowel[i]) {
            return name.slice(0, 4);

        }
    }
    return name;
}
```
```
describe("Example Test Cases", function(){
  Test.assertEquals(nicknameGenerator("Jimmy"), "Jim");
  Test.assertEquals(nicknameGenerator("Samantha"), "Sam");
  Test.assertEquals(nicknameGenerator("Sam"), "Error: Name too short");
  Test.assertEquals(nicknameGenerator("Kayne"), "Kay", "'y' is not a vowel");
  Test.assertEquals(nicknameGenerator("Melissa"), "Mel");
  Test.assertEquals(nicknameGenerator("James"), "Jam");
})
```
**You have passed all of the tests! :)**
