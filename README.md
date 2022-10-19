# personal-code-snippets
Clever code snippets that I'm too lazy to do from scratch again


##Algos
Basic palindrome:
```
var isPalindrome = function(x) {
    return (x.toString() == x.toString().split("").reverse().join(""))
};
or
var isPalindrome = function(x) {
    //Short circuit 
    if(x < 0 || (x !== 0 && x % 10 == 0))
        return false;

    let reverse = 0;
    
    while (x > reverse) {
        reverse = reverse * 10 + x % 10;
        x = ~~(x/10);
    }
    
    return x === reverse || x === ~~(reverse/10);
};
```
